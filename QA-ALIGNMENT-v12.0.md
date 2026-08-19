# QA and Alignment Report - v12.0

**Course:** Mastering Adobe Lightroom for Photo Editing
**Course code:** TGS-2022015367
**QA date:** 19 August 2026
**Result:** PASS

## Identity and source decisions

- The canonical code is `TGS-2022015367`, confirmed by the project folder, legacy v10 deck, live course page, LMS edit record, and target GitHub repository. The shorter code typed in the request was not used.
- The 138-slide v10 deck was treated as the coverage baseline. Its Lightroom ecosystem, workspace, import, organisation, editing, masking, enhancement, collaboration, IP, export, and storage coverage is retained and expanded.
- The approved legacy Assessment Plan was treated as authoritative for instrument structure: six Oral Questioning items (K1-K6) and three Practical Performance tasks (A1-A4).
- The general WSQ process page describes WA + PP/CS and a practice-exam slide. Course-specific evidence and the user's explicit instruction take precedence here: OQ + PP are preserved and no practice exam is included.

## Deliverable gate

| Deliverable | Result | Evidence |
|---|---:|---|
| Trainer deck PPTX/PDF | PASS | 141 slides/pages; 16:9; all-white visual system; editable diagrams; 141 fade transitions |
| Original-deck visual import | PASS | 33 curated original-PPT visual placements embedded across the matching modules |
| Learner Guide DOCX/PDF/Markdown | PASS | 19 PDF pages; seven detailed activity workflows; scenarios, questions, evidence and acceptance criteria |
| Lesson Plan DOCX/PDF | PASS | 6 PDF pages; 6.5 training hours + 1.5 assessment hours; activity slides 45, 46, 99, 100, 101, 102 and 131 verified against `slide_map.json` |
| Individual activity folders | PASS | Seven folders; 36 Markdown files and 36 same-basename PDFs; 23 authorised source images |
| Assessment set | PASS | Four DOCX: OQ paper/key and PP paper/key; independent rendering verifier passed 5/7/7/5 pages |
| Source traceability | PASS | `SOURCE-COVERAGE-v12.0.md` records retained legacy coverage, current expansion, approved sources, image generation and original visual import |
| Public-release boundary | PASS | `.gitignore` excludes `.env`, assessment, references, source assets and build tooling |

## Slide QA

- No shape extends beyond the slide canvas.
- No text run is below 7.5 pt; body text uses the courseware design minimums.
- No blank or broken slide was found in the 141-slide render.
- Two trainer-profile slides are present.
- Digital attendance appears at the front and in the final administration block.
- Briefing for Assessment precedes Assessment Flow.
- The closing order is Assessment (138), Assessment Flow (139), Digital Attendance (140), Thank You (141).
- No practice-exam, mock-exam, step-by-step, or `click the` procedural text occurs in the deck.
- Detailed click-by-click workflows occur only in the Learner Guide and activity packs.

### Visual fix-and-verify cycle

The first independent contact-sheet review identified cropped captions, neighbouring UI fragments, and weak framing on imported legacy screenshots. Slides 20, 23, 35, 38, 50, 56, 59, 62, 65, 71, 83, 95, and 102 were reworked with cleaner source selections or fit-without-crop treatment. The independent second review passed every corrected slide with no remaining publish blocker.

## Cross-artifact alignment

| Competency | Deck and LG coverage | Activity evidence | Assessment evidence |
|---|---|---|---|
| K1 techniques/materials | Topics 1-2 | Activities 01-03, 05-07 | OQ 1; PP Tasks 1-2 |
| K2 tools/equipment | Topic 1 and AI enhancement | Activities 01-02, 06-07 | OQ 2; PP Task 1 |
| K3 workspace | Topic 1 | Activity 01 | OQ 3 |
| K4 theory/context | Topic 2 | Activities 03-06 | OQ 4; PP Task 2 |
| K5 design principles | Topic 2 | Activities 03-07 | OQ 5; PP Tasks 1-2 |
| K6 IP/provenance | Topic 3 | Activity 07 | OQ 6; PP Task 3 |
| A1 stakeholder exploration | Topics 1 and 3 | Activities 01-02, 07 | PP Task 1 |
| A2 practice/experimentation | Topics 1-2 | Activities 01-07 | PP Task 1 |
| A3 capability evaluation | Topic 2 | Activities 03-07 | PP Task 2 |
| A4 production discussion | Topic 3 | Activity 07 | PP Task 3 |

## Assessment QA

- Instrument type, item count, duration and K/A mapping match the approved legacy Assessment Plan.
- Candidate information and instructions precede questions/tasks.
- OQ uses six open-ended questions, one each for K1-K6.
- PP uses three connected tasks mapped to A1/A2, A3 and A4, with embedded authorised source images.
- Answer keys contain suggested evidence and competence indicators.
- Answer keys are trainer-only: they are excluded from GitHub and must not be linked in learner-visible LMS fields.

## Release gates

- Google Drive: PASS. The exact supplied folder ID was dry-run before write. Eight core local/remote MD5 comparisons passed; the Activities tree returned 95 matching files and zero differences. The retained v10 learner PDF was moved to `archive` under a unique retired filename.
- Answer-key privacy: PASS. Both keys were moved into `Assessment/Answer Keys (Trainer Only)`, which has inherited permissions disabled. Their only content permission is the owner; anonymous requests return HTTP 401. OQ and PP candidate papers retain public reader access.
- LMS-TMS: PASS. Course UUID `6e830621-f521-4e01-9956-7e40d58c2a58`, canonical code, title and Drive folder were verified before write. Seven links passed post-write readback and fetch tests; answer-key IDs are absent. Only three topic UUIDs and nine subtopic UUIDs were regenerated by the full-payload sync; all unrelated semantic fields hash-identically before/after after normalising those generated IDs.
- GitHub: publish only learner-facing courseware, activities, README, cover preview, source coverage and this QA report; force-with-lease only against the verified stale `master` SHA `dd1616e1c597410b48dabc50c11b17f6717b490d`.
