# Nested case study: notes for Claude Code

## What this is
A single-page, scroll-driven portfolio case study. Everything (HTML, CSS, JS) is in `index.html`; the only external files are `assets/phone-hero.webp` (hero render) and `assets/phone-brief.webp` (Daily Brief render, used in the solution scene and Dashboard). Fonts load from Google Fonts. No framework, no build step.

## Page order (top to bottom)
1. **Hero** (`#top`, dark): phone balancing on its bottom-left corner; drag spins it around that corner. "Start the day" scrolls to the floating phone in the solution scene.
2. **01 · About the project** (`#next`): light sheet that slides over the hero (curtain).
3. **Before-state** (`#before`): pinned scene, the RM with eight tools around him.
4. **The challenge** (`#challenge`): unnumbered; quote and four questions.
5. **Challenge → solution scene** (`#solution`): pinned; blur-swap text, phone rises, tilts, three pills, flies out, background dissolves to cream.
6. **02 · The solution** (`#features`): Dashboard, Lead pipeline, Incentives (pinned gauge, `#earn`), Communication (`#comm`), with line-diamond-line dividers. Feature labels are NOT numbered.
7. **03 · Design system** (`#dsc`): three rows that slide on scroll.
8. **04 · The AI layer** (`#ai`): pinned five-layer isometric stack with an accordion.
9. **05 · Results / 06 · Next steps** (`#ending`): evening sky, 8 tools collapse into 1, then results, roadmap, thanks, footer on night blue.

## Conventions
- Section numbering is exactly 01 About, 02 Solution, 03 Design system, 04 AI layer, 05 Results, 06 Next steps. Keep it that way unless asked.
- Each section's CSS is grouped and commented in the `<style>` block; JS for each section is its own IIFE at the bottom. Scroll scenes read progress from the section's `getBoundingClientRect()` and are throttled with `requestAnimationFrame`.
- Animate only `transform`, `opacity` and `filter`. Every scene has a `prefers-reduced-motion` fallback; keep it.
- Breakpoints used: 480, 768, 900, 1024. Test at 390 and 1440 wide; there must be no horizontal scroll.
- Two type systems on purpose: site copy is Plus Jakarta Sans (+ Roboto Serif in the hero); anything that is a piece of the app UI uses the app's fonts (Geist, Familjen Grotesk, Geist Mono).
- AI UI must match the product: "AI suggestion · <High|Medium|Low> confidence", confidence bars, "Why this?", signals marked Strong/Medium/Weak, Pending until 2 signals, drafts labelled "not sent".
- Colours: cobalt `#2B4BE0` primary, apricot `#FFB98A` only for emphasis/Hot, amber `#9A6700` for Warm and warnings, cream `#F6F3EE` for the features, night `#0F1F6B` for the ending.

## Known placeholders
- Footer and "Next project / All work / Email / LinkedIn / Design system" links are `#`.
- The challenge quote and its attribution are placeholders; replace with a real RM quote.
- The hero phone render shows "Nallurhalli, Whitefield" (Bengaluru); the rest of the data is Mumbai/Thane.
- Figures in Results (8 tools, ~30 min) come from the original case study.
