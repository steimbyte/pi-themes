# Pi Themes

Unified dark theme collection for **Pi coding agent** & **VSCode/VSCodium**.
Everforest-inspired palette with warm-tinted backgrounds, calibrated for low eye strain.

## Themes

### Pi agent (`pi-themes/`)

Drop-in themes for [Pi coding agent](https://github.com/badlogic/pi-mono).

| File | BG Family | Accent | Description |
|------|-----------|--------|-------------|
| `everforest.json` | neutral dark warm (Everforest Medium) | green `#A7C080` | Canonical Everforest Dark Medium, faithful port |
| `evergreen-soft.json` | soft dark green `#1F3325` | red `#E67E80` | Green BG variant, red-tinted fg (Christmas-feel) |
| `everred-soft.json` | soft dark red `#331F25` | red `#E67E80` | Red BG variant, AAA contrast fg, semantic purple/red diff |
| `gruvbox.json` | near-black warm | orange `#fe8019` | Faithful Gruvbox Dark port |
| `manuscript-dark.json` | warm dark neutral | warm cream | Low-saturation manuscript dark |
| `manuscript-light.json` | warm light | dark warm | Manuscript light counterpart |
| `ccp-manuscript.json` | warm dark neutral | red `#e05555` | CCP-themed manuscript variant |

### VSCode / VSCodium (`themes/`)

Full port with ~300 UI tokens.

| File | Description |
|------|-------------|
| `themes/everred-soft-color-theme.json` | Full VSCode port of everred-soft |

## Install — Pi agent

Copy any JSON from `pi-themes/` to your Pi themes folder:

```bash
# Windows
copy pi-themes\everred-soft.json %USERPROFILE%\.pi\agent\themes\

# macOS / Linux
cp pi-themes/everred-soft.json ~/.pi/agent/themes/
```

Activate via `settings.json`:

```json
{
  "theme": "everred-soft"
}
```

## Install — VSCode / VSCodium

From VSIX (recommended):

1. Install [vsce](https://github.com/microsoft/vscode-vsce): `npm install -g @vscode/vsce`
2. Build: `vsce package`
3. Install: Extensions panel → `...` → "Install from VSIX"

From source:

1. Clone this repo
2. `cp -r themes/ ~/.vscode/extensions/pi-themes/themes/`
3. Symlink `package.json` and `themes/` into your extensions folder, or use `code --install-extension .`

## Highlights

### everred-soft (canonical red variant)

- **BG**: soft dark red `#331F25` (sanft, ~37.7 perceived luminance)
- **FG**: bright salmon `#F5A8AB` — **AAA contrast (8.01)** against bg
- **Diff adds**: strong purple `#B57BDB` (contrast 4.94, AA)
- **Diff removes**: bright red `#FF5555` (contrast 4.84, AA)
- **All accent colors red-tinted** for monochrome coherence
- **Greys replaced** by red-grey tones (`#A87880`, `#8B6068`)

### evergreen-soft (green variant)

- **BG**: soft dark green `#1F3325`
- **FG**: bright salmon `#F5A8AB` (same as everred-soft)
- **Diff adds/removes**: same purple/red as everred-soft
- **toolErrorBg** stays red `#5A1F25` (universal error indicator)
- **Christmas-feel** by design — green BG with warm red-tinted fg

## Source

Originally generated for the Pi coding agent. Everforest palette adapted from
[sainnhe/everforest](https://github.com/sainnhe/everforest) (Dark Medium).

## License

MIT