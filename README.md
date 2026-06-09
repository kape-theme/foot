# ☕ Kape for Foot

Kape is a warm, dark color scheme for **Foot** terminal emulator, rooted in coffee, earth, and amber tones.

## Installation

### Option 1: Manual Installation

1. Create the foot themes directory:
   ```bash
   mkdir -p ~/.config/foot/themes
   ```

2. Copy the theme file:
   ```bash
   cp kape-dark.ini ~/.config/foot/themes/
   ```

3. Include the theme in your foot configuration:
   - Open or create `~/.config/foot/foot.ini`
   - Add the following line in the appropriate section:
     ```ini
     [colors]
     include=~/.config/foot/themes/kape-dark.ini
     ```
   
   Or in the `[main]` section, you can reference it:
   ```ini
   include=~/.config/foot/themes/kape-dark.ini
   ```

4. Reload foot or restart the application

### Option 2: Using Git (Recommended for Updates)

1. Navigate to your foot themes directory:
   ```bash
   cd ~/.config/foot/themes
   ```

2. Clone this repository:
   ```bash
   git clone https://github.com/kape-theme/kape-foot.git kape-foot
   ```

3. Add to your `~/.config/foot/foot.ini`:
   ```ini
   include=~/.config/foot/themes/kape-foot/kape-dark.ini
   ```

4. To update in the future:
   ```bash
   cd ~/.config/foot/themes/kape-foot
   git pull
   ```

## Color Palette

| Color | Normal | Bright |
|-------|--------|--------|
| Black | `#181616` | `#2e2a2a` |
| Red | `#b53535` | `#c94040` |
| Green | `#b4c76e` | `#cad98a` |
| Yellow | `#e7bb5c` | `#f0cc7a` |
| Blue | `#7b8fd4` | `#9aaae0` |
| Magenta | `#b06880` | `#c8889a` |
| Cyan | `#689d8a` | `#89b8a8` |
| White | `#c2c2c2` | `#d4be98` |

See the main [Kape repository](https://github.com/kape-theme/kape) for the complete palette with RGB and HSL values.

## Configuration

### Full Configuration Example

```ini
[main]
font=JetBrains Mono
font-size=11
include=~/.config/foot/themes/kape-dark.ini

[colors]
# Colors are inherited from kape-dark.ini
```

### Overriding Colors

You can override specific colors in your `~/.config/foot/foot.ini` after the include statement:

```ini
[colors]
include=~/.config/foot/themes/kape-dark.ini
# Override specific colors if desired
foreground=d4be98
background=181616
```

## Terminal Features

Kape for Foot includes:

- **Base Colors**: Background, foreground, and cursor
- **Selection Colors**: Highlighted text colors
- **ANSI Colors**: Full 16-color palette (normal and bright)
- **Optimal Contrast**: Designed for readability and comfort

## Customization

To customize the theme, edit `~/.config/foot/themes/kape-dark.ini`. Each section contains:

- `[colors-dark]`: Color definitions for the dark theme

## Troubleshooting

- **Theme not loading**: Check the path in the `include` statement
- **Colors look wrong**: Verify that `kape-dark.ini` is in the correct location
- **Changes not applying**: Restart foot or use the reload function
- **24-bit color issues**: Ensure your terminal supports true color

## Foot Compatibility

This theme is compatible with:
- **Foot 1.13.0+**: Recommended version
- **Earlier versions**: Should work but may have limited functionality

## Contributing

Found an issue or have a suggestion? Open an issue or PR on the [main Kape repository](https://github.com/kape-theme/kape).

## License

MIT © gabiuz
