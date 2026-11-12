# Taiwanese Mahjong — Evidence-Linked Teaching Wiki

An English-only project separate from the earlier AGENTS.md assignment.

## Pages
- [Wiki](index.html): reference-linked cards.
- [Presentation](presentation.html): 12 slides.
- [Run the pipeline](pipeline.html): import, search, check and generate outlines.
- [Workflow](workflow.html): graph, execution notes and reflection.

## Discuss before generating
Target beginner learners; explain the 16-tile resting hand versus a 17-tile standard win, the five-meld-plus-pair rule, tile calls, flowers, and scoring variations.

## Five curated source notes
1. [Mahjong Planet](https://mahjong-planet.com/zh-hant/rules/taiwanese/) — hand, dealer, flowers and site-specific scoring.
2. [Hé Fēn](https://www.hefenmahjong.com/zh-hant/rules/taiwanese) — tiles, winning pattern and scoring.
3. [Mahjong Orchid](https://mahjongorchid.com/en/rules/) — tile families and gameplay.
4. [Mahjong Spot](https://www.mahjongspot.com/rules/tw16/turn-action) — turn actions.
5. [Diamond Mahjong](https://diam.ngct.net/mj_rules.php) — rules and platform variations.

## Reproducible execution
Open pipeline.html and press Run all 4 stages. It imports five embedded English summaries, indexes eight claims, tests the mappings, checks the 16/17 tile distinction, and generates 12 cited slide outlines. Use the search box to retrieve concepts and Download execution log for a timestamped JSON record.

## Known problem and design change
Source materials disagree on some scoring and claim details. The verification step now runs before generation, and failures loop to source retrieval and revision. The main HTML presentation is edited and published separately; the workflow constructs its evidence-linked outline.

## Precise limitation
This site is a deterministic educational Wiki demo, not a live execution of the official LLM Wiki application. The five notes are manually curated summaries; no live LLM API ingest/query/lint, automated full-page scraping, or autonomous correction runs in the webpage. The lesson copy was developed with AI assistance, then checked against linked source references. To satisfy a requirement for the official LLM Wiki engine, run the tool separately with a configured OpenRouter or Ollama model and ingest five documents.
