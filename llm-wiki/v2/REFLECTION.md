# Workflow, Validation and Reflection

## Graph

1. **Discuss** → define a beginner audience, coverage and error criteria.
2. **Collect** → review five separately cited public rules references and prepare English study notes.
3. **Ingest** → load each of the five Markdown files.
4. **Generate Wiki** → AI-authored concepts are saved in `wiki.json`, each with source IDs.
5. **Retrieve** → search relevant Wiki chapters by teaching question.
6. **Validate** → check source IDs, key 16/17-tile concepts, and a scoring-variation caveat. On failure, return to the source/Wiki and revise before generating slides.
7. **Generate HTML lesson** → presentation reads `wiki.json` and builds twelve slides, with source links.
8. **Review** → inspect output and update if a concept is confusing.

## What repeats?

- On an unsupported or missing claim, revise the Wiki entry and rerun validation.
- On a confusing teaching explanation, update the relevant Wiki chapter and reload the HTML lesson.
- The **Test failure → fix → revalidate** button demonstrates the failure branch with a deliberately injected unsupported absolute scoring claim. It reports the rejected statement, restores the source-qualified Wiki claim, and checks again.

## What actually went wrong?

The easiest mistake was turning a **site-specific rule** into an alleged universal Taiwanese rule. Scoring and kong-claim restrictions vary between documented platforms. It would be incorrect to state that every Taiwanese mahjong table uses the same scoring.

## What changed?

The design was first conceived as a final-slide accuracy review. The validation condition was moved to **before slide construction**, where the knowledge base is checked for a scoring variation notice. The lesson now reads the validated Wiki directly rather than keeping an unrelated hard-coded explanation.

## Actual evidence

On 2026-11-12, five Markdown files and ten Wiki chapters were read back from GitHub. Every chapter referenced valid source IDs. Both in-page JavaScript programs passed syntax compilation. A negative-control copy replaced the scoring caveat with an absolute claim; that test was rejected. All checks passed on the retained original Wiki. See `validation-record.json`.

Browser runtime validation for the new v2 pages still requires opening the published GitHub Pages links and clicking Run. The earlier v1 site's working screenshots are not proof of v2 runtime.

## Limitations

The Wiki and program were AI-authored in ChatGPT and run as a deterministic browser implementation. The repository does not use an external hosted LLM API, autonomous LLM validation, or the official `llm-wiki` application's ingest command. Do not describe the negative-control test as proof that an LLM independently discovered an error: it checks a specified rule.
