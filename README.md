```
npm i
npx parcel bundle bundle.js
```

This loads up `tailwindcss/tailwind.css` that comes with its npm package with the content of,
```
@tailwind base;

@tailwind components;

@tailwind utilities;
```
but this ends up having `dist/bundle.css` without parsing those directives.

Instead, by using a locally saved `./tailwind.css` file with the exact same content and specifiying that instead in `bundle.js`, it gets parsed and produces a proper `dist/bundle.css`.
