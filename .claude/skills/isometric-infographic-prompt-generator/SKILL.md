---
name: isometric-infographic-prompt-generator
description: Generate detailed AI image prompts for technical infographics in isometric 3D perspective style. Use when the user wants to create prompts for Gemini, DALL-E, Midjourney, or other AI image generators to produce tech-focused isometric diagrams showing interconnected concepts, architecture diagrams, workflows, or system overviews with futuristic visual styling.
---

# Isometric Infographic Prompt Generator

Generate optimized prompts for AI image generators (Gemini, DALL-E, Midjourney) to create technical infographics in isometric 3D perspective with futuristic aesthetics.

## Core Workflow

1. **Gather requirements** - Understand the topic, key concepts, and relationships
2. **Structure the content** - Organize into central element + connected nodes
3. **Generate the prompt** - Apply the isometric infographic template
4. **Output the prompt** - Provide ready-to-use prompt for target AI model

## Prompt Generation Process

### Step 1: Analyze User Input

Extract from user request:
- **Main topic/title** (central element)
- **Key concepts** (numbered nodes, typically 6-12)
- **Brief descriptions** for each concept
- **Relationships/connections** between concepts
- **Target AI model** (Gemini, DALL-E, Midjourney, etc.)

### Step 2: Apply Template Structure

Use this master template, adapting to user content:

```
[STYLE DECLARATION]
Technical infographic in isometric 3D perspective, futuristic digital aesthetic

[CENTRAL ELEMENT]
Large central [SHAPE: cube/hexagon/platform] with title "[MAIN_TITLE]" and subtitle "[SUBTITLE]"

[NODES - arrange around center]
[For each concept 1-N]:
- Node [N]: "[CONCEPT_TITLE]" - [BRIEF_DESCRIPTION]
  Visual: [ICON/VISUAL_ELEMENT] on illuminated isometric platform

[CONNECTIONS]
Glowing data streams/pathways connecting all nodes to central element
Circuit board pattern in background

[COLOR SCHEME]
Primary: Deep navy/dark blue background (#0a1628 to #1a2744)
Accents: Cyan (#00d4ff), purple (#8b5cf6), pink (#ec4899) neon glows
Platforms: Light gray/white with blue edge lighting
Text: White primary, cyan/purple for highlights

[LIGHTING]
Soft ambient glow, neon accent lighting on edges
Holographic/ethereal quality on data streams

[COMPOSITION]
Central element prominently placed, nodes distributed evenly
Clear visual hierarchy with numbered labels
Professional, clean layout suitable for presentations
```

### Step 3: Customize for Target Model

**For Gemini Nano/Pro:**
- Use natural language descriptions
- Include "high quality", "detailed", "professional"
- Specify aspect ratio (16:9 recommended)

**For DALL-E 3:**
- Be explicit about style and composition
- Use "digital art", "3D render" terminology
- Include negative prompts if needed

**For Midjourney:**
- Add parameters: `--ar 16:9 --style raw --v 6`
- Use "::" for emphasis weighting
- Keep prompt concise but descriptive

## Visual Element Reference

See [references/visual-elements.md](references/visual-elements.md) for:
- Icon suggestions per concept type
- Platform design variations
- Connection style options

## Example Prompts

See [references/example-prompts.md](references/example-prompts.md) for complete prompt examples.

## Output Format

Deliver the generated prompt in a clean code block, followed by:
1. Brief explanation of design choices
2. Suggested modifications for variations
3. Tips for the specific AI model being used
