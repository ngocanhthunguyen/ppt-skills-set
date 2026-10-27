# PowerPoint Skills Set

Twenty custom skills for **Copilot in PowerPoint**, written, tested and refined as part of a university capstone project.
Each skill is a `SKILL.md` file that tells Copilot how to do one job on a deck (fix a slide, build a deck from a brief, check accessibility and so on) and what it must never do (invent numbers, drop caveats, claim something is approved).

## What is in this repo

| Item | What it is |
|---|---|
| `ppt-skills-v2.1/` | The 20 skills, one folder each, each with a `SKILL.md`. **Start here.** |
| `PowerPoint-Skills-Revised-v2.xlsx` | One-page summary: each skill's name, level, what it is for, the prompt to use, and the test result. |

## Use a skill

1. Copy a skill folder (for example `ppt-skills-v2.1/fix-this-slide/`) into your Copilot skills location. The folder name must match the `name:` in the file.
2. Open a deck in PowerPoint and ask Copilot in plain words that name the skill:

   `Use the fix-this-slide skill. Fix slide 4.`

3. Read the reply, then save the deck and check the changes yourself.

The skills are 6,000 to 10,700 characters long, which is more than the 1,024-character Instructions box in the "Create manually" form. Load them from files rather than pasting them into the form.

## Results

Each skill was tested in Copilot in PowerPoint on a planted synthetic deck, and the saved file was checked, not only Copilot's reply.

**16 Pass, 4 Partial Pass, 0 Fail.**

| Partial Pass | Known limit |
|---|---|
| `doc-to-deck` | Faithful content, but titles are not in title placeholders and charts get generic alt text. |
| `executive-summary-slide` | Check every figure: one test merged two different metrics into one sentence. |
| `sensitive-data-scan` | Strong scan. After a redaction the reply is brief, so ask Copilot to list the findings that remain. |
| `translate-deck` | Company and project names and a few meanings were mistranslated. Add a do-not-translate list to the prompt and have a fluent speaker review. |

Nine skills were rewritten after the first round of tests (version 2.1.0); the other eleven are unchanged from 2.0.0.

## Things to know

- **Copilot adds its own questions** (audience, delivery, visual style) and sometimes gives a shorter reply than a skill asks for. Wording in the skills reduces this but cannot remove it.
- **Always save the deck and check the file.** In testing, a reply sometimes said a change was made that the file did not show.
- Tests attached each `SKILL.md` to the chat. Loading the skills through the Copilot skills folder is the intended use and was not tested separately.

## Data and credits

- All test data and examples are **synthetic**. No real organisation, customer or personal data is used anywhere in this repo.
- About half of the skills started from the community repo `heyitsgoad/copilot-playground` (MIT licence) and were rewritten and extended. The rest were written for this project.
- This is a student project. It is not an official Microsoft product or recommendation.
