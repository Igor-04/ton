# Imports cleaned: version suffixes removed

I normalized import specifiers to remove any `@<version>` suffixes like:
- `vaul@1.1.2` -> `vaul`
- `sonner@2.0.3` -> `sonner`
- `recharts@2.15.2` -> `recharts`

This change affects *only* import paths and any Vite alias keys that included versions. Design and functionality were left intact.

## How to run locally

1. Make sure you have Node.js 18+ installed:
   - `node -v` -> should show v18 or newer (v20 recommended)

2. Install dependencies at the project root (where `package.json` is):
   ```bash
   npm install
   ```

3. Start the dev server:
   ```bash
   npm run dev
   ```

4. Open the URL Vite prints in the terminal (usually `http://localhost:5173`).

## Build for production

```bash
npm run build
npm run preview
```

If deploying to GitHub Pages with Vite, ensure `base` is set to `/<repo-name>/` in your `vite.config`.