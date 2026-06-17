# course-graph-trio — SIGCSE TS paper

LaTeX source for the paper on the AI-assisted course-design checker built in
`~/work/projects/course_graph_trio/` (the three-graph backwards-design tool).

## Build

```
make           # pdflatex -> bibtex -> pdflatex x2  ->  main.pdf
make clean
```

`acmart.cls` and `ACM-Reference-Format.bst` are vendored in this directory, so
no system TeX package install is needed (the class is not in the local TeX
tree). `acmart.cls` was built from CTAN source (acmart **v2.18**, 2026/05/31);
the `.dtx`/`.ins` source is gitignored.

## Format (SIGCSE TS 2027 CFP)

- ACM **sigconf** 2-column format, US Letter. Do **not** alter fonts/margins.
- **Double-anonymized.** The 2027 CFP says do **not** use the `anonymous` class
  option — keep visible author blocks under the title with identifying info
  removed, reserving space (4 lines/author, 3 blocks/row). Compiled with
  `[review]` only; the `\author` blocks are anonymized by hand.
- Body **≤ 6 pages**; references may use a 7th page.
- Targeting the **Experience Reports and Tools (ERT)** track.
- At submission: all authors need **ORCiD IDs**; select **3–7 topics** in the
  submission system (separate from the `\keywords` here).
- Conference: **Feb 17–20, 2027, Sacramento, CA**. Deadlines: abstract
  **Jun 26, 2026**, full paper **Jul 3, 2026**, notification **Sep 14, 2026**.

CFP: <https://2027.sigcse-ts.acm.org/track/sigcse-ts-2027-Papers-1>

## Camera-ready checklist

1. Remove `review` from the `\documentclass` options in `main.tex`.
2. Fill in the real `\author` / `\affiliation` / `\email` blocks.
3. Restore the copyright/DOI/ISBN block (`\setcopyright`, `\acmDOI`,
   `\acmISBN`) and re-enable `printacmref`.
4. Verify the `refs.bib` entries marked `% TODO`.

## Status

Scaffold + abstract/intro drafted; remaining sections are skeletoned with
`% TODO` notes drawn from the project's `docs/overview.md` and
`evaluation/study-design.md`. Evaluation results are **not** yet collected —
do not report numbers until the study runs.
