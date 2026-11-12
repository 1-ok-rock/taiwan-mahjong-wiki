# Discussion Before Generation — Decision Record

This is a summary of decisions made in the actual assignment conversation, not a fabricated verbatim chat transcript.

## Initial goal

Create an English-only **Taiwanese 16-Tile Mahjong** learning resource for someone who has never played. The user approved this topic and requested all assignment artifacts in English. The user also wanted the work to reuse the previous GitHub project instead of creating another repository.

## Questions discussed before writing the new Wiki

**Which subject should the Wiki cover?** The beginner rules of Taiwanese 16-tile Mahjong, building on an earlier student RAG experiment.

**Who should learn from it?** Complete beginners using English.

**What should the lesson explain?** The hand size, normal winning pattern, tile families, turns, chi/chow, pung, kong, flower replacement, scoring variations, and a worked example.

**What must not be confused?** Taiwanese 16-tile Mahjong must not be presented as Japanese Riichi Mahjong. The standard waiting hand has sixteen structural tiles, while a normal winning configuration has seventeen.

**How should disagreements be handled?** Identify the source platform, preserve evidence IDs, and present scoring and claim restrictions as ruleset-dependent when sources differ. Do not invent universal numbers.

**What evidence should the assignment show?** At least five individually stored source notes, an evidence-linked AI-authored Wiki, a Wiki-powered HTML lesson, a graph with a genuine recheck branch, a runnable check and reflection on moved validation.

## Outcome of discussion

The resulting files are:

- `sources/S01.md` through `sources/S05.md`: five distinct English study documents.
- `wiki.json`: ten AI-authored Wiki chapters with explicit source IDs.
- `index.html`: Wiki, fetch-based ingestion, search, validation and a deliberate negative-control test.
- `presentation.html`: twelve teaching slides dynamically reading the Wiki.
- `validation-record.json`: independent source and code checks, including a failing negative-control statement.

## AI and implementation disclosure

ChatGPT generated the Wiki text and the implementation code with evidence from linked public rules pages. The deployed webpage runs deterministic processing; it does not run an external LLM API, scrape full articles, or claim to be the official LLM Wiki application. Ingesting five notes here means fetching five separate, prepared Markdown files.

A real LLM-to-Wiki authoring step occurred in this conversation, but not as a repeatable hosted model API inside the GitHub Pages site. Please make this distinction in the submission.
