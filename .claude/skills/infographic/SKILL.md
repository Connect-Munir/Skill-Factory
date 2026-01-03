---
name: infographic
description: Create professional, visually stunning infographics with minimalistic icons and excellent presentation. Use when Claude needs to create infographics, data visualizations, visual summaries, process diagrams, comparison charts, timelines, statistical graphics, or any visual content that presents information clearly. Specializes in clean design, readable typography, and iconic representations.
---

# Infographic Creation Skill

Create professional infographics with minimalistic icons, clean layouts, and highly readable typography. Output formats: SVG (preferred), HTML, React, or image files.

## Design Philosophy

### Core Principles

1. **Clarity First**: Every element serves a purpose. Remove visual clutter.
2. **Minimalistic Icons**: Simple, geometric shapes. No ornate details.
3. **Typography Hierarchy**: Establish clear reading order through size, weight, and spacing.
4. **White Space**: Generous breathing room between elements.
5. **Visual Flow**: Guide the eye naturally from top-to-bottom or left-to-right.

### Mandatory Design Rules

- **Maximum 3 fonts** (1 display, 1 body, 1 accent optional)
- **Maximum 4-5 colors** in palette
- **Consistent spacing units** (8px grid system)
- **Icons at uniform size** within sections
- **Text never smaller than 12px** for readability

## Typography Guidelines

### Font Selection

Use legible, professional fonts. Prioritize readability over aesthetics.

**Recommended Display Fonts** (titles, headers):
- Poppins (geometric, modern)
- Montserrat (versatile, professional)
- DM Sans (clean, contemporary)
- Outfit (friendly, readable)
- Plus Jakarta Sans (elegant, modern)

**Recommended Body Fonts** (content, labels):
- Source Sans Pro (highly readable)
- Nunito Sans (soft, approachable)
- Work Sans (neutral, professional)
- Open Sans (universally readable)
- Lato (warm, humanist)

**Avoid**: Decorative fonts, script fonts, novelty fonts, fonts with poor character spacing.

### Typography Hierarchy

```
Title:          28-36px, Bold (700), uppercase optional
Section Header: 20-24px, SemiBold (600)
Subheader:      16-18px, Medium (500)
Body Text:      14-16px, Regular (400)
Labels/Caption: 12-14px, Regular (400)
Data Numbers:   18-24px, Bold (700) for emphasis
```

### Line Spacing

- **Headlines**: 1.1-1.2 line-height
- **Body text**: 1.5-1.6 line-height
- **Labels**: 1.3-1.4 line-height

## Color Palette Strategy

### Building Your Palette

1. **Primary**: Main brand/theme color (used for key elements)
2. **Secondary**: Supporting color (backgrounds, containers)
3. **Accent**: Highlight color (CTAs, important data)
4. **Neutral Dark**: Text and borders (#1a1a2e to #2d3748)
5. **Neutral Light**: Backgrounds (#f8fafc to #ffffff)

### Proven Palettes

**Corporate Professional**:
```css
--primary: #2563eb;    /* Blue */
--secondary: #f1f5f9;  /* Light Gray */
--accent: #f59e0b;     /* Amber */
--text: #1e293b;       /* Slate */
--bg: #ffffff;         /* White */
```

**Modern Minimal**:
```css
--primary: #18181b;    /* Near Black */
--secondary: #fafafa;  /* Off White */
--accent: #22c55e;     /* Green */
--text: #3f3f46;       /* Dark Gray */
--bg: #ffffff;         /* White */
```

**Warm & Approachable**:
```css
--primary: #ea580c;    /* Orange */
--secondary: #fef3c7;  /* Cream */
--accent: #0891b2;     /* Teal */
--text: #292524;       /* Stone */
--bg: #fffbeb;         /* Warm White */
```

**Data-Focused**:
```css
--primary: #6366f1;    /* Indigo */
--secondary: #e0e7ff;  /* Light Indigo */
--accent: #ec4899;     /* Pink */
--text: #1e1b4b;       /* Dark Indigo */
--bg: #fefefe;         /* Pure White */
```

### Color Accessibility

- Maintain **4.5:1 contrast ratio** for body text
- Maintain **3:1 contrast ratio** for large text (18px+)
- Never rely on color alone to convey meaning
- Test with colorblind simulation tools

## Minimalistic Icon Design

### Icon Style Rules

1. **Stroke-based** preferred over filled (cleaner look)
2. **2-3px stroke width** for consistency
3. **Rounded caps and joins** for friendliness
4. **24x24px or 32x32px** base size
5. **Single color** per icon (use primary or accent)

### Icon Categories & Patterns

**Data/Statistics**:
- Bar chart: 3-4 vertical rectangles of varying height
- Pie chart: Circle with 2-3 segments
- Line chart: Simple ascending/descending line with 2-3 points
- Growth: Arrow pointing upward at 45°

**Process/Flow**:
- Step: Numbered circle
- Arrow: Simple chevron or line with head
- Connection: Dotted or solid line
- Checkpoint: Circle with checkmark

**People/Users**:
- Person: Circle head + rounded body silhouette
- Group: 2-3 overlapping person shapes
- User: Circle with shoulders curve below

**Objects**:
- Document: Rectangle with corner fold
- Lightbulb: Simple bulb outline (ideas)
- Gear: Circle with 6 teeth (settings/process)
- Calendar: Grid rectangle with header bar

### Icon Creation Pattern (SVG)

```svg
<svg width="24" height="24" viewBox="0 0 24 24" fill="none" 
     stroke="currentColor" stroke-width="2" 
     stroke-linecap="round" stroke-linejoin="round">
  <!-- Icon paths here -->
</svg>
```

### Icon Libraries

When using external icons, prefer:
- **Lucide** (clean, consistent)
- **Feather Icons** (minimal, elegant)
- **Heroicons** (well-designed outline set)

## Layout Patterns

### Standard Infographic Layouts

**Vertical Flow** (most common):
```
┌─────────────────────────┐
│        TITLE            │
│       Subtitle          │
├─────────────────────────┤
│  ┌─────┐  ┌─────┐      │
│  │Icon │  │Icon │      │
│  │Stat │  │Stat │      │
│  └─────┘  └─────┘      │
├─────────────────────────┤
│     Section Header      │
│  ┌───────────────────┐  │
│  │   Content Block   │  │
│  └───────────────────┘  │
├─────────────────────────┤
│     Key Takeaway        │
│        Footer           │
└─────────────────────────┘
```

**Timeline/Process**:
```
┌─────────────────────────────────────┐
│              TITLE                  │
├─────────────────────────────────────┤
│  ○──────○──────○──────○──────○     │
│  │      │      │      │      │     │
│ Step1  Step2  Step3  Step4  Step5  │
└─────────────────────────────────────┘
```

**Comparison**:
```
┌─────────────────────────────────────┐
│              TITLE                  │
├─────────────┬───────────────────────┤
│   Option A  │      Option B         │
├─────────────┼───────────────────────┤
│  Feature 1  │     Feature 1         │
│  Feature 2  │     Feature 2         │
│  Feature 3  │     Feature 3         │
└─────────────┴───────────────────────┘
```

**Statistics Dashboard**:
```
┌─────────────────────────────────────┐
│              TITLE                  │
├───────────┬───────────┬─────────────┤
│   [42%]   │   [128]   │   [$5.2M]   │
│  Metric 1 │  Metric 2 │   Metric 3  │
├───────────┴───────────┴─────────────┤
│           Main Chart                │
├─────────────────────────────────────┤
│         Key Insights                │
└─────────────────────────────────────┘
```

### Spacing Guidelines

- **Section gaps**: 40-60px
- **Element gaps**: 16-24px
- **Text to icon**: 8-12px
- **Padding (containers)**: 24-32px
- **Margin (page)**: 40-60px

## Implementation Workflow

### Step 1: Content Analysis

Before design, extract:
1. **Key message**: What's the ONE takeaway?
2. **Data points**: Numbers, percentages, comparisons
3. **Categories**: How to group information
4. **Hierarchy**: What's most important?

### Step 2: Structure Planning

1. Choose layout pattern (vertical, timeline, comparison, etc.)
2. Define sections (3-5 max for clarity)
3. Assign visual weight (size indicates importance)
4. Plan icon usage (1 icon per concept)

### Step 3: Design Execution

1. Set up color palette as CSS variables
2. Import fonts via Google Fonts or local
3. Create base grid (8px system)
4. Build sections top-to-bottom
5. Add icons after text is placed
6. Apply consistent spacing

### Step 4: Refinement

1. Check text readability (zoom out test)
2. Verify color contrast
3. Align elements to grid
4. Remove unnecessary elements
5. Test at target size

## Output Formats

### SVG (Preferred for Quality)

Create standalone SVG files with embedded fonts or web-safe fonts. Use `viewBox` for scalability.

```svg
<svg xmlns="http://www.w3.org/2000/svg" 
     viewBox="0 0 800 1200" 
     width="800" height="1200">
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap');
    .title { font-family: 'Poppins', sans-serif; font-size: 32px; font-weight: 700; }
    .body { font-family: 'Poppins', sans-serif; font-size: 14px; font-weight: 400; }
  </style>
  <!-- Content here -->
</svg>
```

### HTML (Interactive)

Use for web embedding with hover effects and responsive design.

### React (Component-Based)

Build reusable infographic components with props for data.

### Image Export

Convert SVG to PNG/JPG using:
```bash
# Using Playwright/Puppeteer for high-quality rendering
# Or LibreOffice for batch conversion
```

## Quality Checklist

Before delivering, verify:

- [ ] Title is clear and prominent
- [ ] All text is readable at intended size
- [ ] Icons are consistent in style and size
- [ ] Colors meet accessibility standards
- [ ] White space is balanced
- [ ] Visual hierarchy guides the eye
- [ ] No orphaned text (single words on lines)
- [ ] Alignment is precise (use grid)
- [ ] Brand/source attribution included
- [ ] File size is optimized

## Common Mistakes to Avoid

1. **Too many fonts** → Stick to 2-3 max
2. **Cluttered layout** → Embrace white space
3. **Inconsistent icons** → Use single icon set
4. **Poor contrast** → Test accessibility
5. **Tiny text** → Minimum 12px
6. **No visual hierarchy** → Size indicates importance
7. **Overused effects** → No gradients, shadows unless intentional
8. **Data without context** → Add labels and comparisons

## Example Code Patterns

See `references/` for:
- `svg-templates.md`: Ready-to-use SVG structures
- `icon-library.md`: Common icon SVG paths
- `color-palettes.md`: Extended color combinations
