# Excalidraw Generator

A Claude Code skill for generating professional Excalidraw diagrams directly from natural language descriptions. Create beautiful, ready-to-use `.excalidraw` files without manual drawing.

## Features

- **Multiple Diagram Types**: Flowcharts, Architecture Diagrams, UML Class Diagrams, Mind Maps
- **Dual Visual Styles**: Professional mode (clean, polished) and Hand-drawn mode (sketch-style)
- **Smart Layout**: Automatic layout calculation with precise spacing and alignment
- **Direct File Output**: Generates `.excalidraw` files ready to open in Excalidraw
- **Multi-language Support**: Works with both English and Chinese descriptions

## Installation

### Method 1: Marketplace (Recommended)

```bash
# Step 1: Add the marketplace
/plugin marketplace add lexiaoyao20/excalidraw-generator

# Step 2: Install the skill
/plugin install excalidraw-generator@excalidraw-generator
```

### Method 2: Manual Installation

```bash
# Clone and copy to Claude skills directory
git clone https://github.com/lexiaoyao20/excalidraw-generator.git
cp -r excalidraw-generator/skills/excalidraw-generator ~/.claude/skills/
```

Restart Claude Code to load the skill.

## Usage & Examples

Simply ask Claude to create diagrams using Excalidraw. Here are some examples with their generated outputs:

### Flowchart
```
"用 Excalidraw 画一个用户登录流程图"
"Create an Excalidraw flowchart for user login process"
```
![Flowchart Example](images/flowchart.png)

### Architecture Diagram
```
"用 Excalidraw 画一个 iOS MVVM 架构图"
"Generate an Excalidraw architecture diagram for MVVM pattern"
```
![iOS MVVM Architecture](images/MVVM.png)

### UML Class Diagram
```
"用 Excalidraw 画一个 UIView 的类图"
"Draw an Excalidraw UML class diagram for UIView"
```
![UML Class Diagram](images/uiview_class_diagram.png)

### Android Architecture
```
"用 Excalidraw 画一个 Android MVI 架构图"
"Create an Excalidraw diagram for Android MVI architecture"
```
![Android MVI](images/Android_MVI.png)

### Style Options

| Style | When to Use | How to Request |
|-------|-------------|----------------|
| **Professional** (Default) | Technical docs, presentations | Just describe what you need |
| **Hand-drawn** | Brainstorming, informal sharing | Add "手绘风格" or "hand-drawn style" |

Example for hand-drawn style:
```
"用 Excalidraw 画一张手绘风格的流程图"
"Create a hand-drawn style Excalidraw diagram"
```

## Supported Diagram Types

| Type | Description | Use Case |
|------|-------------|----------|
| **Flowchart** | Process flows, decision trees | Algorithm visualization, business processes |
| **Architecture** | System designs, component diagrams | Software architecture, infrastructure |
| **UML Class** | Class hierarchies, relationships | Object-oriented design |
| **Mind Map** | Concept maps, brainstorming | Ideas exploration, knowledge mapping |

## Opening Generated Files

1. Go to [excalidraw.com](https://excalidraw.com)
2. Click **Open** → **Open from your computer**
3. Select the generated `.excalidraw` file (or drag & drop)

## Repository Structure

```
excalidraw-generator/
├── .claude-plugin/
│   └── marketplace.json        # Marketplace configuration
├── skills/
│   └── excalidraw-generator/
│       ├── SKILL.md            # Main skill instructions
│       ├── assets/             # Template files
│       └── references/         # Format specification
├── images/                     # Example screenshots
├── README.md
└── LICENSE
```

## Technical Details

### Layout Calculation

```
textHeight = fontSize × 1.25 × numberOfLines
containerHeight = headerSection + attributesSection + methodsSection
```

### Color Palettes

| Mode | Primary | Success | Warning | Accent |
|------|---------|---------|---------|--------|
| Professional | `#e7f5ff` | `#ebfbee` | `#fff9db` | `#f3f0ff` |
| Hand-drawn | `#a5d8ff` | `#b2f2bb` | `#ffec99` | `#d0bfff` |

## Contributing

Contributions welcome! Feel free to report issues, submit PRs, or suggest new features.

## License

MIT License

## Acknowledgments

- Built for [Claude Code](https://claude.ai/code) by Anthropic
- Uses [Excalidraw](https://excalidraw.com) format specification
