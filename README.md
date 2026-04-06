# HTML PPT Generator

Transforms plain text drafts into beautiful, interactive HTML presentations using reveal.js and Tailwind CSS.

## Overview

This skill takes plain text content and converts it into professional, interactive HTML presentations. It leverages [reveal.js](https://revealjs.com/) for the presentation framework and [Tailwind CSS](https://tailwindcss.com/) for styling.

## Features

- **Reveal.js powered** - Full-featured presentation framework with slide transitions, navigation controls, and progress indicators
- **Tailwind CSS styling** - Utility-first styling for clean, maintainable code
- **Interactive components** - Click-to-reveal cards, tab navigation, expandable sections, interactive flow diagrams, draggable elements, and quizzes
- **Responsive design** - Presentations adapt to different screen sizes
- **Gradient backgrounds** - Multiple color themes (purple, cyan, emerald, orange, slate)
- **Icon support** - Font Awesome icons throughout

## Interactive Components

| Component | Description |
|-----------|-------------|
| Click-to-Reveal Cards | Expand cards to show hidden details |
| Tab Navigation | Switch between content panels |
| Interactive Flow Diagrams | Clickable process/step sequences |
| Expandable Lists | Accordion-style Q&A sections |
| Interactive Quizzes | Multiple choice with feedback |
| Draggable Elements | Drag-and-drop sorting activities |

## Usage

This skill is designed to be used with Claude Code. When you provide content for a presentation, the skill will:

1. Analyze the content thoroughly
2. Plan the slide structure
3. Generate the HTML with Tailwind CSS styling
4. Review and refine the output
5. Iterate until the presentation meets quality standards

## Project Structure

```
html-ppt-generator/
├── SKILL.md    # Main skill documentation
└── README.md   # This file
```

## Technical Details

### External Dependencies (via CDN)

- Tailwind CSS
- Reveal.js (CSS + JS)
- Font Awesome
- Google Fonts (Inter, Noto Sans SC)

### Design Principles

1. **Tailwind-first** - All styling uses utility classes; custom CSS only for animation keyframes
2. **Reveal.js compatible** - Avoids CSS properties that conflict with reveal.js
3. **Content-centered** - Each slide centers content with proper max-width constraints
4. **Full-screen** - Presentations fill the entire browser viewport

## License

MIT
