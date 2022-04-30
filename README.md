## react-flow nocss vite

Repro repository of an error when importing react-flow-renderer styles.

### How to simulate the error
```bash
npm install
npm run dev
```

### How to fix
Add the css files to the `exports` field in the package.json
```javascript
{
  "exports": {
    /// ...
    "./dist/style.css": "./dist/style.css",
    "./dist/theme-default.css": "./dist/theme-default.css"
  }
}
```