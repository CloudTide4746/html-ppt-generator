---
name: html-ppt-generator
description: |
  Generate HTML-based PowerPoint presentations from text drafts. Use this skill whenever the user wants to create a presentation, slideshow, or PPT from raw text content. The user might say things like "帮我做个PPT"、"生成幻灯片"、"create a presentation"、"把这段话做成演示文稿"、"输入草稿生成HTML幻灯片"。This skill analyzes the content structure and produces a professional, visually impressive HTML presentation using reveal.js and Tailwind CSS.
---

# HTML PPT Generator

Transforms plain text drafts into beautiful, interactive HTML presentations using reveal.js and Tailwind CSS.

## Core Principle

All visual styling uses Tailwind CSS utility classes. Custom CSS is only used for complex animation keyframe definitions. This approach keeps the code readable and maintainable.

---

## CRITICAL: Execution Timing Requirements

**This skill MUST NOT rush to output results. Follow the timing guidelines below:**

| Phase | Minimum Time | Purpose |
|-------|-------------|---------|
| Content Analysis | 60+ seconds | Thoroughly understand all content |
| Slide Planning | 60+ seconds | Plan each slide structure |
| Code Generation | 90+ seconds | Write clean, correct code |
| Review & Fix | 90+ seconds | Check for bugs, fix issues |
| Iteration Cycle | 60+ seconds per iteration | Test and refine |

**Total minimum time before first output: 5 minutes**

**You MUST wait between phases. Do not skip steps. Do not rush.**

---

## Workflow

### Phase 1: Deep Content Analysis (MANDATORY - 60+ seconds)

Before generating any HTML, thoroughly analyze the input content. Read through it multiple times and understand:

1. **Main Topic and Title** - What is the core message? What is the presentation about?
2. **Key Sections** - Group related points together. How many major topics are there?
3. **Logical Hierarchy** - What is the flow from introduction to conclusion? What builds on what?
4. **Content Density** - How much text is there per section? Dense content needs simpler layouts
5. **Content Type** - Is this technical, creative, business, or academic content? This affects color themes and visual style
6. **Interactive Opportunities** - Which concepts would benefit from clickable expansion, tabs, or interactive diagrams?
7. **Content to Slide Mapping** - How many slides are needed? What content goes on each slide?

**Think through these questions carefully:**
- What is the narrative arc of this presentation?
- Where can interactivity help audience understanding?
- What visual metaphors would work best for this content?
- Are there comparisons, processes, or lists that need special layout treatment?

**Spend adequate time on this step. Rushing leads to poor layout decisions and centering bugs.**

### Phase 2: Strategic Slide Planning (MANDATORY - 60+ seconds)

Plan EACH slide BEFORE writing code. For each slide, document:

```
Slide N: [Slide Title]
- Layout type: [describe the layout structure]
- Content elements: [what goes on this slide - headings, body, icons, interactive components]
- Background theme: [purple | cyan | emerald | slate | orange - describe the gradient direction]
- Key visual: [what icon, diagram, or visual element is the focus]
- Interactive features: [clickable cards | tabs | expandable sections | quiz | diagram]
- Centering approach: [describe how content will be centered within the slide]
```

**Layout Type Guidelines:**

| Content Pattern | Recommended Layout |
|----------------|-------------------|
| Title + intro text | Centered hero layout with tags below title |
| 2-3 key points | Card grid with 2 or 3 columns |
| Comparison (A vs B) | Side-by-side comparison cards |
| Process or steps | Horizontal flow diagram with arrows between steps |
| Benefits and limitations | Two or three column layout showing pros/cons/impact |
| Summary with takeaways | Icon cards plus a closing quote |
| Q&A discussion | Centered layout with discussion prompt cards |

**Think about for each slide:**
- How will the content be centered on the slide?
- What max-width should the content container have?
- How much padding is appropriate?
- Will elements wrap on smaller screens?
- How many interactive elements per slide?

### Phase 3: Code Generation (MANDATORY - 90+ seconds)

Generate the HTML following the patterns described in later sections. Key focus areas:

1. **Proper Centering Structure** - Every slide must use the inner flex container pattern for true centering
2. **Consistent Padding** - Use moderate padding values, not excessive
3. **max-width Containers** - Limit content width with centered containers
4. **Interactive Components** - Add proper click handlers for all interactive elements
5. **Consistent Theming** - Each slide has its own gradient background that fills the screen

### Phase 4: Review & Self-Check (MANDATORY - 90+ seconds)

**Check ALL of the following before considering the output ready:**

#### Centering Verification:
- Does each section have proper full-screen sizing and flex layout?
- Does the inner wrapper properly center content both vertically and horizontally?
- Does the content container use max-width with horizontal centering?
- Is padding moderate (not excessive)?
- Are nested grids properly contained within the centered wrapper?

#### Reveal.js Compatibility:
- Are there any forbidden CSS properties that would break reveal.js?
- Are the controls and progress bar visible?
- Do transitions work smoothly?

#### Interactive Components:
- Are all click handlers properly implemented in JavaScript?
- Does tab switching work correctly?
- Do expandable sections toggle properly?
- Can flow diagram steps be clicked and highlighted?

#### Visual Quality:
- Does each slide have a gradient background?
- Is gradient text used for key headings?
- Do cards have proper transparency and borders?
- Are icons consistent in size throughout?

### Phase 5: Iteration & Refinement (MANDATORY - 60+ seconds per iteration)

**After initial generation, you MUST iterate at least once:**

1. **First Iteration**: Review the code for centering issues. Check each slide's structure. Fix any layout problems.
2. **Second Iteration**: Ensure interactive components work. Verify all JavaScript functions are complete. Add any missing functionality.
3. **Third Iteration** (if needed): Polish visual details. Ensure color consistency across slides. Check typography hierarchy.

**For each iteration:**
- Read through the generated code carefully
- Identify one specific issue to fix
- Make the fix
- Verify the fix didn't break anything else

**Do not output the final result until you have gone through at least 2 review iterations.**

---

## CRITICAL: Full-Screen Display & Centering Requirements

**The presentation MUST fill the entire screen. Incorrect centering is the most common bug. Follow these rules EXACTLY.**

### The Centering Problem Explained

The most common mistake is using full-width containers with excessive horizontal padding. This defeats centering because the content stretches to fill the available space instead of being centered within a constrained width.

**What goes wrong:**
- Using `w-full` with lots of padding makes content fill the entire width
- Content that should be centered ends up aligned to the left
- Grids and cards don't appear centered within the slide

**The correct approach:**
- Use an inner flex container that fills the slide and centers content
- Constrain content width with max-width
- Center the max-width container horizontally with auto margins
- Use moderate padding, not excessive amounts

### Centering Structure for Each Slide

Each slide section should follow this structure:

1. **The section element** - Sized to fill the screen with flex layout
2. **Inner wrapper** - Fills available space and centers content both axes
3. **Content container** - Constrained width that is centered horizontally

**Key Centering Rules:**

1. **Section element**: Must have full-screen sizing with flex layout for stacking
2. **Inner wrapper**: Uses flex layout to fill available space and center content both vertically and horizontally. Uses moderate padding for spacing.
3. **Content container**: Constrains width using max-width, fills that width with w-full, and centers horizontally with auto margins. Uses moderate padding, not excessive amounts.
4. **Nested grids**: Use full width within the content container, which keeps them centered
5. **Avoid excessive padding**: Moderate padding values work best; too much padding breaks centering
6. **Use relative sizing**: Percentages or standard Tailwind sizing units, not fixed pixel values

---

## Required External Resources

The presentation requires these CDN resources:

- **Tailwind CSS** - For styling
- **Reveal.js** - For presentation framework (CSS and JavaScript)
- **Font Awesome** - For icons
- **Google Fonts** - For typography (Inter for English, Noto Sans SC for Chinese)

### Tailwind Configuration

Define custom colors (primary indigo, secondary purple, accent cyan, dark slate backgrounds) and font families in the Tailwind config. The config should be placed in a script tag before the closing head tag.

### Reveal.js Initialization

Initialize Reveal.js with: centered positioning, no margins, full width and height, visible controls and progress, slide transitions with fade background transition.

---

## Layout Patterns

### Pattern 1: Centered Hero (Title Slide)

For title slides with a single main message. The content sits in the center of the slide with a constrained width. An icon appears above the title. Tags or labels appear below the subtitle. Everything is centered horizontally.

### Pattern 2: Centered Content with Grid Cards

For slides with multiple points or cards. The heading is centered at the top. Below it, a grid of cards spans the content area. Each card has an icon, title, and description. The entire grid is centered within the slide.

### Pattern 3: Flow Diagram

For explaining processes or sequences. Steps are arranged horizontally with arrows between them. Each step is a card with an icon and label. The flow wraps on smaller screens using flex wrapping. Steps can be interactive and highlight when clicked.

---

## Interactive Component Patterns

### Click-to-Reveal Cards

A card that shows a title and icon by default. When clicked, additional detailed content expands below the title. The chevron icon rotates to indicate expanded state. Use this for information that supplements the main content.

**Behavior**: Click toggles visibility of hidden details. Icon rotates 180 degrees when expanded.

### Tab Navigation

A row of buttons that act as tabs. Clicking a tab shows its corresponding content panel while hiding others. The active tab has different styling to indicate selection. Use this when presenting alternative views of the same topic.

**Behavior**: Only one tab's content is visible at a time. Active tab has highlighted styling.

### Interactive Flow Diagram

A horizontal sequence of steps connected by arrows. Each step is a clickable card. When clicked, that step becomes highlighted with a border and background change. Use this for processes, algorithms, or sequences.

**Behavior**: Clicking a step highlights it with colored border and background. Previous highlights are removed.

### Draggable Elements

A container with draggable elements inside. Elements can be picked up and moved. When dragging, the element becomes semi-transparent. Use this for interactive sorting or grouping activities.

**Behavior**: Elements can be dragged. Visual feedback during drag operation.

### Expandable List Items

A vertical list where each item can be expanded. Clicking an item reveals hidden content below it. A plus icon changes to minus when expanded. Use this for FAQs or detailed explanations.

**Behavior**: Click toggles expansion. Icon switches between plus and minus.

### Interactive Quiz

A question with multiple choice answers. Clicking an answer provides immediate feedback - correct answers show green, incorrect show red. Use this for knowledge checks or engagement.

**Behavior**: Clicking an answer highlights it with colored ring and shows feedback message.

---

## Visual Design Guidelines

### Backgrounds

Each slide should have a dark gradient background. Use one of these themes:
- Purple theme: indigo to purple to slate
- Cyan theme: cyan to blue to indigo
- Emerald theme: emerald to teal to cyan
- Orange theme: orange to red to rose
- Slate theme: slate to indigo to purple

The gradient should be applied directly to each slide section.

### Gradient Text

For main headings, use gradient text (purple to cyan across the text). This creates visual interest and draws attention to key titles.

### Cards

Cards should have semi-transparent white backgrounds with subtle borders. Use consistent padding and border radius. Cards can have icons, titles, and descriptive text.

### Icons

Icons should be from Font Awesome. Use consistent sizing within similar contexts. Icons can be colored to match the theme (blue, purple, green, cyan, etc.).

---

## Reveal.js Compatibility Rules

**Forbidden on slide sections:**
- Display flex with important flag - this conflicts with reveal.js
- Fixed viewport height - reveal.js manages height internally
- Overflow hidden - this causes content to disappear
- Minimum viewport height - conflicts with reveal.js scaling
- Clamp in font sizes - conflicts with reveal.js scaling

**Required on slide sections:**
- Full screen width and height sizing
- Flex column layout for vertical stacking
- Inner wrapper with flex centering for content positioning

---

## Code Style Requirements

1. Use Tailwind classes for all styling - avoid custom CSS
2. Use semantic HTML elements appropriately
3. Use id attributes for JavaScript targeting
4. Comment complex sequences in the code
5. Only use CDN resources - no local file dependencies

---

## Final Checklist Before Output

**Verify ALL items before declaring the presentation complete:**

### Centering Verification:
- Each slide section has full-screen sizing with flex layout
- Inner wrapper uses flex centering for both axes
- Content containers use max-width with horizontal centering
- No excessive padding values on content wrappers
- Grids inside content containers use full width

### Reveal.js Compatibility:
- No forbidden CSS properties on slides
- Controls and progress bar are visible
- Transitions between slides work smoothly

### Interactive Components:
- All click handlers have corresponding JavaScript functions
- Tab switching logic is complete and functional
- Toggle and expand functionality works correctly

### Visual Quality:
- Consistent gradient backgrounds across slides
- Gradient text on main headings
- Proper card styling with transparency
- Icon sizes are consistent throughout

### File Output:
- File is saved to the correct path
- File opens in a browser without errors
- All CDN resources load correctly

---

## Anti-Patterns to Avoid

1. **Excessive padding on content wrappers** - This breaks centering. Use moderate values.
2. **Full width without centering on containers** - Without auto margins, full width just stretches content
3. **Mini theater animations** - Do not create small animation boxes in slides
4. **Split layouts** - Do not put content on left and demo on right in a small box
5. **Auto-playing animations** - Users should control all interactions
6. **Fixed height containers inside slides** - Use relative sizing
7. **External background divs** - Each slide has its own full background
8. **Rushing to output** - Follow the timing requirements strictly

You MUST perform a second pass focused purely on UI/UX refinement before final output.
