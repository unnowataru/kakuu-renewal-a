# GitHub Pages Prep (Pattern A)

## Current status
- Site root is ready: `index.html`, `styles.css`
- Jekyll disabled: `.nojekyll`
- Branch publish mode ready: `main` branch root deployment
- Legacy brand token scan completed: no hits in file paths or content

## Publish plan
1. Initialize a Git repository in `C:\dev\kakuu-renewal-a` (if not already).
2. Push this directory to a GitHub repository as the `main` branch.
3. Enable Pages with source `main` branch and `/ (root)` path.
4. Wait for Pages build to complete.
5. Verify published URL and run final visual QA on desktop/mobile.

## Pre-publish checks
```powershell
$legacy = -join ([char[]](110,101,116,119,111,114,108,100))
rg -n -i -uuu $legacy C:\dev\kakuu-renewal-a
Get-ChildItem -Recurse -Force C:\dev\kakuu-renewal-a | Where-Object { $_.FullName -match $legacy }
```
