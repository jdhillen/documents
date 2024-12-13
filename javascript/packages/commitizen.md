# Commitizen Setup Guide

A guide for setting up commitizen in your project to standardize commit messages using conventional commits.

## Installation

```bash
# Install commitizen and conventional changelog adapter
npm install --save-dev commitizen cz-conventional-changelog
```

## Configuration

### 1. Initialize commitizen with conventional changelog
```bash
npx commitizen init cz-conventional-changelog --save-dev --save-exact
```

### 2. Add script to package.json
```json
{
  "scripts": {
    "commit": "cz"
  }
}
```

### 3. Add commitizen configuration
```json
{
  "config": {
    "commitizen": {
      "path": "./node_modules/cz-conventional-changelog"
    }
  }
}
```

## Usage

Instead of using `git commit`, use:
```bash
git add .
npm run commit
```

This will prompt you for:
1. Type of change you're committing:
   - feat: A new feature
   - fix: A bug fix 
   - docs: Documentation only changes
   - style: Changes that don't affect the meaning of the code
   - refactor: A code change that neither fixes a bug nor adds a feature
   - perf: A code change that improves performance
   - test: Adding missing tests
   - chore: Changes to the build process or auxiliary tools

2. Scope of the change (optional)
3. Short description
4. Longer description (optional)
5. Breaking changes (optional)
6. Issues affected (optional)

## Example Commit Flow
```
? Select the type of change that you're committing: feat
? What is the scope of this change? (press enter to skip) auth
? Write a short, imperative mood description of the change: add OAuth2 login support
? Provide a longer description of the change: (press enter to skip)
? Are there any breaking changes? yes
? Describe the breaking changes: new environment variables required for OAuth
? Does this change affect any open issues? yes
? Add issue references (e.g. "fix #123", "re #123".): closes #31
```

Results in commit message:
```
feat(auth): add OAuth2 login support

BREAKING CHANGE: new environment variables required for OAuth

closes #31
```

## Git Hooks (Optional)

To enforce using commitizen, you can set up a Git hook:

1. Install husky:
```bash
npm install --save-dev husky
```

2. Add prepare script:
```json
{
  "scripts": {
    "prepare": "husky install"
  }
}
```

3. Add commit-msg hook:
```bash
npx husky add .husky/prepare-commit-msg "exec < /dev/tty && npx cz --hook || true"
```

## VS Code Integration

Install the "Commitizen Support" extension for VS Code to use commitizen directly from the editor.

## Benefits
- Standardized commit messages
- Automatic changelog generation
- Better commit history readability
- Easier version management
- Improved collaboration

## Common Issues

### "Command not found: cz"
Make sure you've installed dependencies and are using `npm run commit` instead of just `cz`.

### "Git hooks not executing"
Check that husky is properly installed and initialized:
```bash
npm run prepare
```

### "Error: Path not found"
Verify your package.json commitizen config points to the correct path:
```json
{
  "config": {
    "commitizen": {
      "path": "./node_modules/cz-conventional-changelog"
    }
  }
}
```

## Additional Resources
- [Commitizen GitHub](https://github.com/commitizen/cz-cli)
- [Conventional Commits](https://www.conventionalcommits.org/)
- [Husky](https://typicode.github.io/husky/)