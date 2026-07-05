# Terminal Workbench for Windows Terminal

A calm, dense, high-contrast theme for Windows Terminal — graphite backgrounds, restrained ANSI-style accents, and matching window chrome, in dark and light modes. Not retro green-on-black novelty: the interface stays quiet and color is spent only on signal.

A port of the [Terminal Workbench](https://github.com/Real-Fruit-Snacks/terminal-workbench) Obsidian theme, built from its [portable design spec](https://github.com/Real-Fruit-Snacks/terminal-workbench/blob/main/docs/THEME-SPEC.md).

## What's included

[`terminal-workbench.json`](terminal-workbench.json) contains:

- **Terminal Workbench** — dark color scheme
- **Terminal Workbench Light** — light color scheme
- Matching **window themes** (tab row / chrome) for both modes

## Install

1. Open Windows Terminal → Settings (<kbd>Ctrl</kbd>+<kbd>,</kbd>) → **Open JSON file**.
2. Copy both entries from the `schemes` array of [`terminal-workbench.json`](terminal-workbench.json) into the `schemes` array of your `settings.json`.
3. Copy both entries from the `themes` array into the top-level `themes` array of your `settings.json` (create the array if it doesn't exist).
4. Activate the dark theme:

```jsonc
{
    "theme": "Terminal Workbench",
    "profiles":
    {
        "defaults":
        {
            "colorScheme": "Terminal Workbench"
        }
    }
}
```

Color schemes apply to open tabs immediately; the window theme (tab row chrome) applies after closing and reopening Windows Terminal.

### Light mode

Swap both names for their `Light` counterparts:

```jsonc
"theme": "Terminal Workbench Light",
"colorScheme": "Terminal Workbench Light"
```

## Palette

### Dark

| Slot | Hex | | Slot | Hex |
|---|---|---|---|---|
| background | `#090C0D` | | foreground | `#DCE4DF` |
| black | `#202A2F` | | brightBlack | `#63736F` |
| red | `#FF6E7A` | | brightRed | `#FF7F8A` |
| green | `#63F2AB` | | brightGreen | `#76F4B5` |
| yellow | `#F0C674` | | brightYellow | `#F2CD85` |
| blue | `#74A8FF` | | brightBlue | `#85B2FF` |
| purple | `#B78CFF` | | brightPurple | `#C09AFF` |
| cyan | `#6BDCFF` | | brightCyan | `#7DE0FF` |
| white | `#B4C3BD` | | brightWhite | `#DCE4DF` |
| cursor | `#63F2AB` | | selection | `#1B3A2D` |

### Light

| Slot | Hex | | Slot | Hex |
|---|---|---|---|---|
| background | `#F5F7F4` | | foreground | `#17201D` |
| black | `#17201D` | | brightBlack | `#60706A` |
| red | `#C8324C` | | brightRed | `#B42D44` |
| green | `#007A4D` | | brightGreen | `#006E45` |
| yellow | `#A46600` | | brightYellow | `#945C00` |
| blue | `#2E62B8` | | brightBlue | `#2958A6` |
| purple | `#7357B8` | | brightPurple | `#684EA6` |
| cyan | `#006F9E` | | brightCyan | `#00648E` |
| white | `#C8D5CF` | | brightWhite | `#F5F7F4` |
| cursor | `#007A4D` | | selection | `#CBE2D8` |

## Notes

- The dark selection color is deliberately quiet (accent at ~20% over the background, per the design spec). If you prefer a more visible selection, change `selectionBackground` to `#204836`.
- Normal ANSI colors are the spec's exact accent tokens; bright variants are the same hues lifted ~12% in dark mode and deepened ~10% in light mode, so bold text stays distinguishable without turning the palette into a rainbow.
- The ANSI blue slot (the one color the spec doesn't define) uses a steel blue that sits between the cyan accent and the violet keyword color.

## License

[MIT](LICENSE)
