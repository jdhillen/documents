# Semantic Release Setup Guide

A comprehensive guide for setting up semantic-release in your project to automate version management and package publishing.

## Installation

```bash
# Install semantic-release and essential plugins
npm install --save-dev semantic-release @semantic-release/changelog @semantic-release/git @semantic-release/npm @semantic-release/github
```

## Configuration

### 1. Create Configuration File
Create `.releaserc.js` in your project root:

```javascript
export default {
  branches: ['main'],
  plugins: [
    '@semantic-release/commit-analyzer',
    '@semantic-release/release-notes-generator',
    '@semantic-release/changelog',
    ['@semantic-release/npm', {
      'npmPublish': true
    }],
    '@semantic-release/github',
    ['@semantic-release/git', {
      'assets': ['package.json', 'CHANGELOG.md'],
      'message': 'chore(release): ${nextRelease.version} [skip ci]\n\n${nextRelease.notes}'
    }]
  ]
};
```

### 2. Add Script to package.json
```json
{
  "scripts": {
    "semantic-release": "semantic-release"
  }
}
```

### 3. Setup GitHub Action
Create `.github/workflows/release.yml`:

```yaml
name: Release
on:
  push:
    branches:
      - main

jobs:
  release:
    name: Release
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
        with:
          fetch-depth: 0
      
      - uses: actions/setup-node@v4
        with:
          node-version: '20'
          registry-url: 'https://registry.npmjs.org'
          scope: '@your-scope'

      - name: Install dependencies
        run: npm ci

      - name: Release
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
          NODE_AUTH_TOKEN: ${{ secrets.NPM_TOKEN }}
        run: npx semantic-release
```

## Token Setup

### GitHub Token
1. Go to GitHub → Settings → Developer settings → Personal access tokens
2. Generate new token with:
   - repo (full)
   - write:packages
   - read:packages

### NPM Token
1. Go to npmjs.com → Access Tokens
2. Generate new token (Automation)
3. Save token

### Add Tokens to GitHub Secrets
1. Go to your repository → Settings → Secrets → Actions
2. Add `NPM_TOKEN` with your npm token
3. Add `GITHUB_TOKEN` (usually automatically available)

## Usage

Semantic Release uses your commit messages to determine the next version number and generate changelogs. Use conventional commits:

```bash
feat(scope): add new feature
fix(scope): fix some bug
docs(scope): update documentation
style(scope): format code
refactor(scope): refactor code
perf(scope): improve performance
test(scope): add tests
chore(scope): update build tasks
```

Version bumps are determined by:
- `fix:` → Patch release (1.0.1)
- `feat:` → Minor release (1.1.0)
- `BREAKING CHANGE:` → Major release (2.0.0)

## Local Testing

Test your semantic-release setup locally:
```bash
NPM_TOKEN=your-npm-token GITHUB_TOKEN=your-github-token npx semantic-release --dry-run
```

## Common Issues

### Release Not Triggering
- Verify commit messages follow conventional format
- Check GitHub Action logs
- Verify tokens have correct permissions

### NPM Publishing Fails
- Check NPM_TOKEN permissions
- Verify package.json has correct name and version
- Check if package name is available on npm

### Git Errors
- Ensure GITHUB_TOKEN has correct permissions
- Check branch configuration in .releaserc.js
- Verify git remote is correctly set

## Integrations

### With Commitizen
```bash
npm install --save-dev commitizen cz-conventional-changelog
```

Add to package.json:
```json
{
  "scripts": {
    "commit": "cz"
  },
  "config": {
    "commitizen": {
      "path": "./node_modules/cz-conventional-changelog"
    }
  }
}
```

### With Husky
```bash
npm install --save-dev husky @commitlint/cli @commitlint/config-conventional
```

Create `.commitlintrc.js`:
```javascript
export default {
  extends: ['@commitlint/config-conventional']
}
```

## Project Structure
```
your-project/
├── .github/
│   └── workflows/
│       └── release.yml
├── .releaserc.js
├── .commitlintrc.js
├── CHANGELOG.md
└── package.json
```

## Additional Resources
- [Semantic Release Documentation](https://semantic-release.gitbook.io/)
- [Conventional Commits](https://www.conventionalcommits.org/)
- [GitHub Actions](https://docs.github.com/en/actions)