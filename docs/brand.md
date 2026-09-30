# Dracula for Astryx brand reference

This theme is dark-only and follows the [Dracula specification](https://spec.draculatheme.com/) and [contribution guidelines](https://draculatheme.com/contribute). The distributed `theme.css` and `tokens.css` files expose the palette through Astryx and plain CSS tokens.

## Palette

| Role               | Hex       | Use                                 |
| ------------------ | --------- | ----------------------------------- |
| Background         | `#282A36` | Page background                     |
| Current line       | `#6272A4` | Line highlights and visible borders |
| Selection          | `#44475A` | Selected rows and quiet surfaces    |
| Background light   | `#343746` | Cards and surfaces                  |
| Background lighter | `#424450` | Popovers and floating elements      |
| Background dark    | `#21222C` | Shadows and dark foregrounds        |
| Foreground         | `#F8F8F2` | Primary text on dark surfaces       |
| Comment            | `#6272A4` | Disabled and muted text             |
| Cyan               | `#8BE9FD` | Information and secondary links     |
| Green              | `#50FA7B` | Positive and success states         |
| Orange             | `#FFB86C` | Warnings and attention              |
| Pink               | `#FF79C6` | Decorative accents                  |
| Purple             | `#BD93F9` | Primary actions, links, and titles  |
| Red                | `#FF5555` | Negative and error states           |
| Yellow             | `#F1FA8C` | Tags and chips                      |

## Semantic colors

- Purple identifies primary actions, links, and unvisited titles.
- Green represents positive and success states.
- Red represents negative and error states.
- Yellow identifies tags and chips.
- Cyan represents information and secondary links.
- Orange represents warnings.
- Pink is reserved for decorative emphasis.

The theme also includes derived colors for accessible text hierarchy and functional states. These preserve the palette's hues while meeting UI contrast requirements.

## Charts

Categorical series use the nearest Dracula hues: comment blue, orange, purple, green, pink, cyan, and red. Teal uses ANSI bright cyan, indigo uses ANSI bright blue, and brown reuses orange.

Sequential chart ramps provide five lightness steps for purple, pink, red, orange, yellow, teal, blue, shamrock, and gray.

## Syntax highlighting

The syntax theme maps keywords to pink, strings to yellow, comments to comment blue, numbers to orange, functions to green, types to cyan, and variables to foreground.

## Status surfaces

Banners, badges, and alerts use muted background tokens with semantic accent borders. Text on solid status fills uses background dark rather than black.

Focus and interactive edges use the accent color. Cards, banners, badges, and progress bars remain static.

## Typography and dimensions

The theme uses JetBrains Mono for body, heading, and code roles.

- Base type: `14px`
- Heading scale: `24px`, `20px`, `17px`, and `14px`
- Supporting text: `12px`
- Main gap: `23px`
- Viewport spacing: `15px`
- Widget content: `15px` vertical and `17px` horizontal
- Border radius: `5px`
