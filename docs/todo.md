# Todo

## Template leftovers to clean up

- [x] Delete `_projects/3_project.md`, `4_project.md`, `5_project.md` — unedited al-folio demo projects with lorem ipsum content and stock photos
- [x] Replace `_data/repositories.yml` — currently lists Torvalds, alshedivat, Bootstrap, jQuery, etc. Replace with your own GitHub repos/users
- [x] Fix `_data/cv.yml` lines 98–101 — remove leftover "Description 3. / Sub-description 1. / Sub-description 2." placeholder text under PhD Education
- [x] Fix `_pages/cv.md` — `cv_pdf: example_pdf.pdf` points to a missing file; add a real CV PDF to `assets/pdf/` or remove the line to hide the download button

## Content gaps

- [x] Fill in `about.md` `subtitle:` field — shown as tagline under your name on the homepage (e.g. *Geospatial Data Engineer · PhD*)
- [x] Add `linkedin_username` in `_config.yml`
- [ ] Update hardcoded years list in `_pages/publications.md` — currently `[2022, 2021, 2020, 2019, 2018, 2017]`, must be updated manually when adding new publications (still matches all years in papers.bib as of this pass — left as-is per decision, revisit next time a pub outside this range is added)

## Unfinished projects

- [x] `_projects/DS_project_ST_release/` — was actually complete content, just missing the `.md` extension so Jekyll wouldn't render it; renamed to `DS_project_ST_release.md`
- [x] `_projects/DS_project_ST_release_S1/` — same issue, renamed to `DS_project_ST_release_S1.md`; also fixed a broken image reference (`interfero.png` → `interfero.jpeg`, the file that actually exists)
