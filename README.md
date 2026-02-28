# dmenu - Dynamic Menu

Application launcher with alpha (transparency) patch.

## Usage

```
dmenu_run [options]
```

## Command-Line Options

| Option | Description |
|---|---|
| `-b` | Show dmenu at the bottom of the screen |
| `-f` | Grab keyboard before reading stdin |
| `-i` | Case-insensitive matching |
| `-l <lines>` | Use vertical list with given number of lines |
| `-m <monitor>` | Show on specified monitor |
| `-p <prompt>` | Set prompt text to the left of input |
| `-P` | Password mode: hide user input |
| `-r` | Reject non-matching input |
| `-fn <font>` | Set font or font set |
| `-nb <color>` | Normal background color |
| `-nf <color>` | Normal foreground color |
| `-sb <color>` | Selected background color |
| `-sf <color>` | Selected foreground color |
| `-v` | Print version |

## Keyboard Shortcuts (Built-in)

| Shortcut | Action |
|---|---|
| `Escape` / `Ctrl+c` | Exit without selecting |
| `Return` / `Ctrl+j` | Confirm selection |
| `Shift+Return` | Confirm input (even if not in list) |
| `Tab` | Copy selection to input |
| `Left` / `Ctrl+b` | Move cursor left |
| `Right` / `Ctrl+f` | Move cursor right |
| `Home` / `Ctrl+a` | Move cursor to start |
| `End` / `Ctrl+e` | Move cursor to end |
| `Up` / `Ctrl+p` | Select previous item |
| `Down` / `Ctrl+n` | Select next item |
| `PageUp` | Select previous page |
| `PageDown` | Select next page |
| `Backspace` / `Ctrl+h` | Delete character before cursor |
| `Delete` | Delete character after cursor |
| `Ctrl+w` | Delete word before cursor |
| `Ctrl+u` | Delete to start of line |
| `Ctrl+k` | Delete to end of line |
| `Ctrl+y` | Paste from primary selection |

## Configuration

| Setting | Default |
|---|---|
| Position | Top of screen |
| Fonts | monospace:size=10, JoyPixels:pixelsize=8 |
| Normal colors | fg: #bbbbbb, bg: #222222 |
| Selected colors | fg: #eeeeee, bg: #005577 |
| Background alpha | 0xe0 (~88%) |
| Word delimiters | Space |

## Patches

- **Alpha**: Transparency support (works embedded in transparent st)
- **Password mode** (`-P`): Hides user input
- **Reject** (`-r`): Reject non-matching input
- Xresources support (pywal compatible)
- Color emoji support (requires libxft-bgra)
- Mouse clickable options

## Integration with dwm

Launched via `Mod+d` in dwm. Inherits colors and font settings from dwm's dmenu configuration.

## Installation

```
sudo make install
```

Requires [libxft-bgra](https://aur.archlinux.org/packages/libxft-bgra/) for color emoji support.
