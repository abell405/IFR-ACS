# IFR-ACS — Instrument Rating ACS study guide

Static site on GitHub Pages: https://abell405.github.io/IFR-ACS/
Pages source: "Deploy from a branch", `main`, `/ (root)`. No build step, no workflow.

## Always push changes
After ANY change (content, layout, README), commit and push to `origin main` right away, without asking. A push is how a change goes live. Tell the user it will be live at the URL above in a minute or two.

## Project layout
- `index.html` is the whole site: HTML, CSS and JS in one file. Same design and markup as the companion PPL-ACS repo.
- Content follows the FAA Instrument Rating – Airplane ACS (FAA-S-ACS-8C), Areas I–VIII, then a Reference section (mock oral, airspace, aeromedical/ADM, performance, IFR altitudes, numbers and formulas, mnemonics, regulations).
- Each section is a `<section class="task" data-area="…" data-title="…">`. The sidebar groups tasks by `data-area`; Area dividers are `.area-h` blocks.
- Each ACS element is a `<details class="el k|r|s" id="IR-I-B-K2a">` with a `.code` label and `.el-b` body. The sidebar and search are built from these automatically, so new elements only need the same markup. Keep `.code` labels short (they don't wrap on phones).
- Tasks end with one or more `.quiz` blocks (`<details>` with the question in `<summary>`, answer in `<p>`; add `<span class="sc">SCENARIO</span>` for scenario questions, `<span class="sc lg">ORAL</span>` in the mock oral).
- Aircraft numbers are for the Piper Pilot 100i (POH page refs in the text). Scenario altitudes and minimums are made up for practice.

## Checks before pushing
- Syntax-check the script (extract the `<script>` body and run `node --check`).
- Keep ACS codes, tolerances, and regulation numbers accurate.
- No horizontal scroll at 390 px width.

## Keep it generic
No organization, school, or author names anywhere (page text, comments, README, commit messages).
