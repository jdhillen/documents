[Remove .DS_Store Files from Git](https://dev.to/mattiadev/gitignore-mac-dsstore-files-even-if-already-committed-14dm)

```bash
// First, unmatch previously committed files
find . -name .DS_Store -print0 | xargs -0 git rm -f --ignore-unmatch

// Then add .DS_Store to .gitignore file
.DS_Store

// Finally, commit and push changes
git commit -m "Update - Remove .DS_Store from everywhere"
git push
```
