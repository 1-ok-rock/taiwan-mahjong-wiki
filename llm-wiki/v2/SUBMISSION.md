# eeclass Submission — English (replace identifying details)

**Title:** NTHU [Student ID] EECS [Full Name] Taiwanese Mahjong LLM Wiki

## 1. Topic and Introduction

My project is **Taiwanese 16-Tile Mahjong: A Beginner's Guide**. Before generation, I discussed the target audience, key concepts, common mistakes and source requirements with ChatGPT. The goal was to help an English-speaking beginner understand hand structure, tile families, gameplay actions, and common rule variations.

## 2. Wiki and Source Ingestion

AI-authored Wiki: https://1-ok-rock.github.io/taiwan-mahjong-wiki/llm-wiki/v2/index.html

Five individual English source-note documents were prepared from cited online rule references (S01–S05). ChatGPT used the sourced notes to compose ten Wiki chapters, each linked to the source IDs. The public page can load the five Markdown files, search the Wiki, and verify its consistency.

## 3. Teaching HTML Presentation

https://1-ok-rock.github.io/taiwan-mahjong-wiki/llm-wiki/v2/presentation.html

The 12-page English presentation reads the Wiki data file directly, so changes to the Wiki appear in the teaching content. Each slide shows the supporting Wiki chapters and evidence source IDs. The explanations cover beginner concepts and include a worked winning-hand example.

## 4. Loop / Graph

Design and reflection: https://github.com/1-ok-rock/taiwan-mahjong-wiki/blob/main/llm-wiki/v2/REFLECTION.md

Discussion → Collect five sources → Ingest → Generate Wiki → Retrieve → Validate → Generate HTML slides → Review.

If validation fails, the process returns to the relevant Wiki source, revises the claim, and runs the check again. I placed validation before slide generation so an unsupported claim does not spread across slides.

## 5. One Execution and Check Result

The repository check on November 12, 2026 confirmed five source documents, ten Wiki chapters, valid citations, relevant 16/17-tile statements and JavaScript syntax. In a negative-control test, an invented universal scoring claim was detected and rejected. The unmodified Wiki passed the checks.

Validation record: https://github.com/1-ok-rock/taiwan-mahjong-wiki/blob/main/llm-wiki/v2/validation-record.json

[Attach a screenshot of the new v2 Wiki displaying its Run / PASS result after opening it.]

## 6. Reflection

The most error-prone step was consolidating different rule sources. Some platforms use different scoring formulas and different restrictions on calls. At first, I planned to review accuracy only after preparing slides. I changed the graph to validate claims and citations before slide generation. This made it easier to catch a mistake once, correct the Wiki, and generate consistent teaching material.

## Tool-Use Disclosure

ChatGPT authored the Wiki and the HTML code from five separately linked, manually curated source-note files. The deployed ingestion/search/validation steps are deterministic and do not call a live external LLM API or the official LLM Wiki application. The five input documents are English study notes, not full downloaded articles.
