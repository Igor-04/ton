# Fix notes (macOS Apple Silicon friendly)

- Removed non-existent package `@stdlib/deploy` from dependencies.
- Ensured Rollup v4 is present and added `@rollup/rollup-darwin-arm64` to devDependencies
  to bypass an npm optional-dependencies issue that causes
  `Cannot find module '@rollup/rollup-darwin-arm64'` on macOS ARM.
- Did not touch any design or application logic.
- Imports were previously normalized to remove version suffixes (e.g., `pkg@1.2.3` → `pkg`).

## Recommended Node version
Use Node 20 LTS for best compatibility:
```
nvm install 20
nvm use 20
```

## Install & run
```
npm install
npm run dev
```
