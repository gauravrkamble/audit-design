# Audit Design Brief for Claude Code

## Objective

You have access to the Figma file. Perform a full audit of all pages, frames, components, and styles, and tell me what issues you can detect and which of those you can solve directly.

## Important

- Do not modify anything yet
- Start in audit mode only
- Inspect the file deeply and systematically
- Focus on issues that affect production readiness, consistency, scalability, and design quality

## Goal

I want to know:

1. What issues exist in the Figma file
2. Which issues you can fix automatically
3. Which issues need my design decision before changing
4. Which issues you cannot safely solve

## Audit Scope

Review the file across these categories.

### 1. Layout and alignment

- Misalignment
- Inconsistent spacing
- Broken grid usage
- Off-center elements
- Uneven paddings and gaps
- Pixel precision issues
- Inconsistent object sizes

### 2. Typography

- Inconsistent font sizes
- Inconsistent line heights
- Inconsistent text styles
- Accidental local overrides
- Baseline alignment issues
- Text containers with bad sizing or padding

### 3. Color and visual system

- Too many colors
- Duplicate or near-duplicate colors
- Missing semantic color tokens
- Inconsistent status colors
- Inconsistent chart color usage
- Inconsistent opacity usage
- Inconsistent gradients
- Inconsistent shadows and effects

### 4. Components and variants

- Duplicate components doing the same job
- Detached instances
- Missing variants
- Inconsistent button, input, and badge states
- Inconsistent icon treatment
- Missing reusable patterns
- Places where components should be created or consolidated

### 5. Auto layout, constraints, and responsive structure

- Frames or groups that should use auto layout but do not
- Frames using auto layout incorrectly
- Broken or unnecessary nested auto-layout wrappers
- Inconsistent padding inside auto-layout frames
- Inconsistent gap values inside stacks and card groups
- Incorrect use of Hug, Fill, and Fixed sizing
- Elements that should resize with content but do not
- Elements that stretch when they should hug content
- Elements that use fixed widths or heights where responsive sizing would be better
- Misaligned row and column stacks
- Incorrect alignment settings inside auto-layout frames
- Space-between used incorrectly
- Absolute-positioned elements that should be part of auto layout
- Constraints fighting against auto layout behavior
- Broken resizing behavior across similar components
- Components that break when text length changes
- Components that break when badges, chips, or status labels change size
- Cards, tables, filters, or nav items that do not respond cleanly to content changes
- Unnecessary wrapper frames or groups making layout harder to maintain
- Places where cleaner auto-layout structure would improve scalability and handoff

### 6. Variables, tokens, and styles

- Hard-coded values that should be tokenized
- Missing color variables
- Missing spacing, radius, and effect tokens
- Inconsistent naming
- Unused or duplicate styles
- Poor token or style structure

### 7. Accessibility and usability

- Poor color contrast
- Touch target issues
- Tiny text
- Weak hierarchy
- Inconsistent states
- Badges or charts that are hard to read

### 8. Charts and data UI

- Inconsistent chart colors
- Semantic mismatch between chart colors and badges
- Unreadable labels
- Poor legend consistency
- Inconsistent card or chart padding
- Overly decorative or noisy data visualization styling

### 9. File hygiene and scalability

- Messy layer naming
- Inconsistent frame naming
- Cluttered page structure
- Hidden junk layers
- Unnecessary duplicates
- Asset inconsistency
- Anything that will make handoff, scaling, or maintenance harder

## Reporting Format

For every issue found, report:

- Issue title
- Category
- Severity: low, medium, or high
- Exact location: page, frame, component, or node
- What is wrong
- Why it matters
- Whether you can fix it directly
- Confidence level: high, medium, or low
- Proposed fix

## Output Structure

Organize the output into these four sections.

### Section A: Issues you can fix safely right now

These should be high-confidence, low-risk fixes such as:

- Spacing cleanup
- Alignment cleanup
- Rounding inconsistent sizes
- Token or style cleanup
- Layer naming cleanup
- Consistent shadows or opacity application
- Text style normalization
- Component consolidation where safe
- Safe auto-layout fixes such as correcting padding, gap, alignment, Hug, Fill, Fixed sizing, redundant wrappers, and simple content-resizing issues where design intent is clear

### Section B: Issues you can likely fix, but should confirm first

These may affect design intent, such as:

- Merging similar colors
- Changing chart palettes
- Restructuring components
- Changing badge semantics
- Introducing a new token system
- Adjusting responsive behavior
- Larger auto-layout restructuring that may affect responsive behavior, component architecture, or intended layout logic

### Section C: Issues you can detect, but should not change without explicit approval

These may include:

- Changing information hierarchy
- Changing UX flow
- Redesigning layout structure
- Changing content strategy
- Changing branding or visual direction

### Section D: Issues you cannot safely solve from the file alone

Examples:

- Business logic ambiguity
- Unclear product requirements
- Unclear data meaning
- Missing product rules for states or permissions

## After the Audit, Provide

1. A concise executive summary
2. The top 10 highest-impact issues
3. A recommended cleanup order
4. A list of quick wins
5. A list of structural improvements
6. A proposed "can fix now" batch vs "needs approval" batch

## Important Constraints

- Do not edit the file during this step
- Do not redesign anything yet
- Do not guess when design intent is unclear
- Be explicit about uncertainty
- Prioritize practical, solvable issues over generic design commentary

## Success Criteria

- I should clearly understand what is wrong in the file
- I should know what you can fix automatically
- I should know what needs my decision
- I should have a clear plan for improving the file efficiently
