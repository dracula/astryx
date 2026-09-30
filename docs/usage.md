# Using Dracula for Astryx

Choose one integration path for each project. See the [installation guide](../INSTALL.md) for package, Git, and manual setup.

## Prebuilt Astryx theme

This is the recommended path for Astryx applications:

```tsx
import "@astryxdesign/core/reset.css";
import "@astryxdesign/core/astryx.css";
import "astryx-dracula/tokens.css";
import "astryx-dracula/theme.css";
import { Theme } from "@astryxdesign/core/theme";
import { astryxDraculaTheme } from "astryx-dracula";

<Theme theme={astryxDraculaTheme} mode="dark">
  <App />
</Theme>;
```

Keep the imports in this order so the theme layer can override the Astryx base styles.

## Plain CSS

Projects that do not use Astryx components can import the standalone token layer:

```css
@import "astryx-dracula/tokens.css";
```

The file defines dark-mode root values with `color-scheme: dark`. Prefer semantic tokens such as `var(--color-primary)`, `var(--color-background)`, and `var(--space-gap)` over raw values.

## Fonts

Copy the package's `fonts/` directory into the directory your application serves at `/fonts/`. For Vite, this is normally `public/fonts/`.

The token layer declares the required `@font-face` rules. If the files are unavailable, text falls back to the system monospace font.

## Migrating an existing project

1. Inventory raw colors, root custom properties, utility classes, and existing theme providers.
2. Map each color to the [brand reference](./brand.md).
3. Remove the old theme provider and conflicting root overrides.
4. Add the Astryx and Dracula imports in the documented order.
5. Replace one-off values with semantic tokens.
6. Build the project and visually verify its key pages.

## Vite layer order

Most applications need no special configuration. If another stylesheet overrides the theme layers, establish the Astryx layer order before loading application styles:

```ts
import react from "@vitejs/plugin-react";
import { defineConfig } from "vite";

export default defineConfig({
  plugins: [
    {
      name: "astryx-css-layer-order",
      transformIndexHtml: () => [
        {
          tag: "style",
          children:
            "@layer reset, priority1, priority2, priority3, priority4, priority5, priority6, priority7, priority8, priority9, astryx-theme;",
          injectTo: "head-prepend",
        },
      ],
    },
    react(),
  ],
});
```

## Troubleshooting

- **Components are unstyled:** Confirm that `reset.css` and `astryx.css` load before the Dracula files.
- **Fonts fall back to monospace:** Confirm that both font files are available under `/fonts/`.
- **Theme colors are overridden:** Remove conflicting root-level `--color-*` declarations and check the CSS import order.
- **Manual installation does not resolve imports:** Keep the distributed files together or update their relative imports for your project structure.

## Theme guidelines

- Do not introduce one-off hex values. Map colors to the documented palette.
- Do not override semantic `--color-*` properties at the application root.
- Prefer component props, followed by theme overrides, over application-specific CSS overrides.
- Use spacing, radius, and color tokens instead of raw values in components.
