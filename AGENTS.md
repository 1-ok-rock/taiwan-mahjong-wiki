# AGENTS.md — Taiwan Mahjong Wiki

## Project mission
Maintain an accessible, beginner-friendly, **English-only** educational website about Taiwanese 16-tile mahjong. The core objective is to make future pages easy to add consistently by an AI coding assistant. No betting, payments, or gambling promotions.

## Non-negotiable language rules
- All visible website text, headings, navigation, buttons, alt text, captions, meta descriptions, examples and references must be English only.
- All README text, code comments and newly added documentation must be English.
- Never add Japanese or Chinese translations or Chinese characters. Use English romanizations such as Chi, Pong, Kong and Tai, and English tile names.
- Every HTML page must start with `<html lang="en">`.

## Technology and structure
- Static HTML5, CSS3 and vanilla JavaScript only. No frameworks, builds, dependencies, backend or API keys.
- Deploy from GitHub Pages using the main branch and repository root.
- Use relative local paths to support /taiwan-mahjong-wiki/ rather than absolute / paths.
- Homepage: `index.html`; articles: `pages/*.html`; shared styles: `assets/style.css`; enhancements: `assets/script.js`.
- Keep the existing navigation and site functional even if JavaScript is disabled.
- Filenames must be lower-case English kebab-case such as `flower-tiles.html`.

## Editorial rules
- Explain the standard resting hand of 16 structural tiles and standard winning hand of 17 structural tiles (five melds plus a pair). A Kong is four physical tiles but one meld; flower tiles are replacement bonus tiles in common variants.
- Identify scoring, winning thresholds, call precedence, special hands and unusual Kong cases as possible house-rule variants.
- Never invent specific scoring awards, rule priorities, citations or links. Prefer verification with two independent reliable references before making new factual claims.
- Every factual article must have a References section with relevant working links; clearly note rules that vary by group.
- Do not reproduce copyrighted diagrams or copy source text. Use original plain-text tile examples.
- Avoid unsupported claims: label uncertain rules as subject to confirmation or omit them.

## Design system
- Palette: dark emerald #123d35, green #186c5b, cream #f6f6ee, gold #cba65a.
- Use the common `.container`, `.article`, `.card`, `.notice`, `.example`, `.tiles`, `.tile`, `.source-list` and `.next` CSS classes.
- Reuse the existing header, menu, footer, breadcrumbs, page width and typography.
- Each page must contain a meaningful unique title and meta description, exactly one h1, a brief introduction, logical h2 headings, real examples if helpful, References, and navigation back to other pages.
- Use semantic HTML, good contrast, visible keyboard focus, readable font sizes, mobile-friendly responsive layouts, accessible input labels.
- Avoid unnecessary animations and third-party assets.

## Required step-by-step AI workflow for adding a page
1. Read this AGENTS.md completely, then inspect index.html, a current article and assets/style.css before coding.
2. Define audience, topic, learning outcomes, sources and house-rule caveats.
3. Name the new file `pages/<lowercase-kebab-case-topic>.html`.
4. Copy the existing article structure; adapt title, meta description, breadcrumbs, heading, introduction, sections, examples, notice and References.
5. Use existing shared CSS; only extend shared styles if truly needed. Never duplicate entire stylesheets.
6. Add a new topic card in the homepage grid and ensure its description is searchable by assets/script.js.
7. Update the global navigation on every page only if the topic warrants a top-level nav item; otherwise use the homepage topic index and article cross-links.
8. Check that paths from article pages use ../ correctly. Do not break existing links or overwrite unrelated files.
9. Test local links, basic HTML structure, page titles, English-only content, responsive behavior around 375px and topic search. Verify external citations when online browsing is available.
10. Summarize every changed file, sources checked, rule variations and actual tests; never claim unperformed tests.

## Acceptance criteria
A new page is complete when it follows the English-only policy, matches the existing design, is linked from the homepage, has source references and suitable rule caveats, works under GitHub Pages subpaths, and does not break existing pages.

## Reuse demonstration
Example prompt: "Read AGENTS.md and add a flower tiles guide. Use the existing English-only page design, provide reliable references and house-rule caveats, add a homepage topic card, and report all changes and tests."

## Academic integrity
Human reviewers should inspect AI-generated content, verify facts, and follow course rules for acknowledging AI help.
