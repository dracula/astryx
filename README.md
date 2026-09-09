# Dracula for Astryx

> A dark theme for [Astryx](https://astryx.atmeta.com/).

![Screenshot](./screenshot.png)

## Install

All instructions can be found at [draculatheme.com/astryx](https://draculatheme.com/astryx).

```bash
bun add astryx-dracula
```

```tsx
import '@astryxdesign/core/reset.css';
import '@astryxdesign/core/astryx.css';
import 'astryx-dracula/tokens.css';
import 'astryx-dracula/theme.css';
import { Theme } from '@astryxdesign/core/theme';
import { astryxDraculaTheme } from 'astryx-dracula';

<Theme theme={astryxDraculaTheme} mode="dark">
  <App />
</Theme>;
```

## Team

This theme is maintained by the following person(s) and a bunch of [awesome contributors](https://github.com/dracula/astryx/graphs/contributors).

| [![yuzu-octopus](https://github.com/yuzu-octopus.png?size=100)](https://github.com/yuzu-octopus) |
| ----------------------------------------------------------------------------------------------- |
| [yuzu-octopus](https://github.com/yuzu-octopus)                                                 |

## Community

- [Twitter](https://twitter.com/draculatheme) - Best for getting updates about themes and new stuff.
- [GitHub](https://github.com/dracula/dracula-theme/discussions) - Best for asking questions and discussing issues.
- [Discord](https://draculatheme.com/discord-invite) - Best for hanging out with the community.

## Dracula PRO

[Dracula PRO](https://draculatheme.com/pro) - Premium color scheme and UI theme designed for programming.

## License

[MIT License](./LICENSE)
