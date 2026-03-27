# Design Review Plugin for Claude Code

A Claude Code plugin that reviews UI/UX designs against professional standards. Based on the [FormFactor design school](https://www.youtube.com/@signartura/videos) methodology — extracted from 46 video lectures and live review sessions.

## Installation

**Add the marketplace:**
```
/plugin marketplace add gregorymm/design-review-plugin
```

**Install the plugin:**
```
/plugin install design-review@formfactor-design
```

## Usage

### Manual invocation

```
/design-review path/to/screenshot.png
/design-review https://www.figma.com/design/...
```

### Auto-trigger

The skill activates automatically when you say things like:
- "review this design"
- "check my layout"
- "give me design feedback"
- "review this screen"
- "check visual hierarchy"

## What It Reviews

The plugin evaluates designs across 7 categories:

### Sizing & Spacing
Checks all sizes against the standard scale (2, 4, 8, 12, 16, 20, 24, 32, 40, 48, 56, 64...). Flags non-standard values like 51px or 46px. Evaluates the proximity rule — related elements should be closer than unrelated ones.

### Visual Hierarchy
Verifies CTA dominance, the rectangle principle (every block fits a clean rectangle), F-pattern scanning flow, and focal point contrast.

### Typography
- Minimum body text: 16px
- Line height: 130-150% (explicitly set, not auto)
- Max 3 text styles per screen
- Max text width: 600px

### Color
Checks for "dirty" mid-range colors, contrast compliance on both light and dark backgrounds, gray palette temperature, and disabled state distinction.

### Alignment & Consistency
Evaluates alignment lines, element consistency (identical or clearly different — never "slightly different"), icon bounding boxes (24x24 or 20x20), and center-alignment limits.

### Layout & Composition
Groups of 3-5 elements, proper grid usage (mobile: 2 columns/16px margins, desktop: 12 columns/32-60px margins), consistent border radius, and minimal divider lines.

### Figma Structure
When reviewing Figma files: auto-layout correctness, component usage, no empty padding wrappers, numeric line heights.

## Portfolio Review Mode

When reviewing a portfolio or case study, additionally evaluates:

- **Case structure**: Problem → Research → Hypothesis → Solution → Results
- **Visual presentation**: Large enough to read? No tilted mockups?
- **Before/After**: Shown near the top of the case?
- **Metrics**: Present and specific?
- **Research conclusions**: Actually drawn, not just artifacts?
- **Red flags**: Text-only portfolios, tiny screenshots, wireframes without final designs

## Feedback Format

Every review follows this structure:

1. **Overall impression** — current state in 1-2 sentences
2. **Critical issues** — must-fix problems with specific pixel values and principles
3. **Improvements** — changes that would elevate the design
4. **What works well** — good decisions acknowledged

## Knowledge Base

The plugin includes a structured knowledge base covering:

| Topic | What's Inside |
|-------|--------------|
| UI/UX Principles | Standard size scale, proximity rule, rectangle principle, F-pattern, whitespace |
| Common Mistakes | Non-standard sizes, auto line-height, dirty colors, ALL CAPS abuse, inconsistency |
| Design Review Criteria | What hiring managers check in the first 5-7 minutes |
| Figma Best Practices | Components, auto-layouts, prototyping, variables/tokens, icons |
| Typography | Size scale, line height, text styles, font recommendations |
| Color Theory | HSL basics, energy levels, palettes, safe zones, dark theme |
| Layout & Composition | Grouping, grids, border radius, mockups, before/after |
| CJM/Wireframes | Process vs action decomposition, information architecture |
| Portfolio Presentation | Structure, case studies, platforms, red flags, NDA handling |

Source: [@signartura](https://www.youtube.com/@signartura/videos) YouTube channel (FormFactor design school). Instructors: Artur (founder), Kirill (design lead at RSHB), Anya (Belka Car), Polina (design systems), Sasha Yushkova (variables/tokens).

## License

MIT
