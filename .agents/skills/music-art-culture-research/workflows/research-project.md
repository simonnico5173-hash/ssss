# Research Project Workflow

## Purpose

Run a complete music, art, culture, or social-science research project from a research question to a paper-style report, while preserving a reproducible audit trail.

## Trigger

Use this workflow when the user asks for a substantial research project, literature-backed investigation, systematic/scoping review, artist/album/artwork study, or cultural-phenomenon analysis.

## Pipeline

`Question → Scope → Search plan → Automatic literature discovery → Metadata normalization → Deduplication → Screening → Citation chasing → Full-text retrieval → Evidence extraction → Evidence quality assessment → Literature synthesis → Analysis → Research gap → Paper draft → Citation audit → Final report`

## Step 1 — Create the project workspace

Create a project directory with:

```text
research-project/
├── research-question.md
├── search-log.md
├── sources.csv
├── screening.md
├── evidence-matrix.md
├── literature-synthesis.md
├── research-gap.md
├── analysis.md
├── references.bib
├── audit.md
└── final-paper.md
```

If the host agent has file/project tools, create these files before substantive research. Do not fabricate empty research results; mark files as pending when appropriate.

## Step 2 — Define the research question

Write:
- primary research question;
- secondary questions;
- object/population/corpus;
- geographic and historical scope;
- time range;
- relevant disciplines;
- inclusion/exclusion criteria;
- intended output and audience.

Convert vague prompts into answerable research questions before searching.

## Step 3 — Build the search plan

Generate several query families:
- exact terms;
- synonyms and spelling variants;
- historical terminology;
- names of artists, works, movements, institutions, genres, scenes, or places;
- theory and method terms;
- competing explanations;
- review/systematic-review terms.

Record every actual query and search date in `search-log.md`.

## Step 4 — Automatic literature discovery

When external access is available, search multiple scholarly sources as appropriate:

1. OpenAlex — broad discovery and citation graph.
2. Crossref — DOI and bibliographic verification.
3. Semantic Scholar — scholarly discovery, references, citations, and related papers.
4. Google Scholar/JSTOR/library databases — use only when legitimately accessible.
5. Discipline-specific indexes.
6. Museums, archives, universities, government bodies, publishers, artists, labels, and institutional collections for primary/contextual sources.

Run multiple query families instead of relying on one query.

Important: never claim that a database or API was searched unless it was actually accessed. Record the database, query, date, and result count when available.

## Step 5 — Normalize and deduplicate

For every discovered source capture:

`title | authors | year | venue | DOI | URL | abstract | keywords | source type | database | citation count | relevance | notes`

Deduplicate in this order:
1. exact DOI;
2. normalized title + first author + year;
3. manual review of near-duplicates.

Prefer authoritative metadata when records conflict.

## Step 6 — Screen sources

Classify each candidate as:
- Include
- Exclude
- Maybe

Record a reason for every exclusion or unresolved decision. Apply the criteria consistently.

For substantial reviews, preserve the screening trail so another researcher could understand how the corpus was assembled.

## Step 7 — Citation chasing

For high-value sources:
- inspect backward references;
- inspect forward citations;
- identify seminal works;
- identify major critiques/replies;
- identify recent replications, extensions, or revisions.

Add newly discovered sources to the same screening process rather than bypassing it.

## Step 8 — Retrieve full text

Prefer:
1. publisher full text;
2. institutional repository;
3. legal open-access copy;
4. library-provided access;
5. abstract/metadata only when full text is unavailable.

Do not present an abstract-level claim as if the full paper was read. Record access limitations.

## Step 9 — Build the evidence matrix

For each included source record:

`Source | Question | Data/Object | Method | Main finding | Evidence | Limitation | Relevance | Confidence`

Separate:
- what the source explicitly reports;
- what the researcher interprets;
- what is inferred beyond the source.

For quotations, preserve exact wording and page/section information when available.

## Step 10 — Evaluate evidence quality

Assess:
- source authority;
- methodological fit;
- transparency;
- sample/corpus adequacy;
- alternative explanations;
- limitations and biases;
- consistency with other sources;
- whether the evidence is primary, secondary, or tertiary.

Do not equate citation count with truth or methodological quality.

## Step 11 — Synthesize the literature

Organize the literature by:
- schools/traditions;
- theoretical frameworks;
- major findings;
- methodological differences;
- disagreements;
- historical change;
- evidence strength;
- unresolved questions.

Write `literature-synthesis.md` as an argument map, not a list of paper summaries.

## Step 12 — Identify the research gap

Explicitly distinguish:
- genuinely under-researched questions;
- questions with conflicting evidence;
- populations/regions/periods underrepresented;
- methodological gaps;
- theoretical gaps;
- data/source gaps.

Avoid claiming that a topic is "never studied" unless the search supports that statement.

## Step 13 — Analyze

Choose methods appropriate to the question and evidence.

Possible approaches include:
- musicological/formal analysis;
- ethnomusicology;
- art-historical analysis;
- cultural studies;
- sociology/anthropology;
- thematic/content/discourse analysis;
- comparative case study;
- historical/archival analysis;
- interviews/ethnography when data are available;
- quantitative descriptive analysis;
- computational text/audio/image analysis when justified.

Clearly separate description, interpretation, and inference.

## Step 14 — Draft the paper

Write `final-paper.md` using this structure:

1. Title
2. Abstract
3. Research Question and Scope
4. Method and Search Strategy
5. Literature Review
6. Theoretical/Conceptual Framework
7. Evidence and Analysis
8. Competing Interpretations and Counterevidence
9. Discussion
10. Limitations and Evidence Gaps
11. Conclusion
12. References
13. Appendices: Search Log and Evidence Matrix

Every major factual or scholarly claim should be traceable to evidence.

## Step 15 — Bibliography

Generate `references.bib` from verified metadata. Prefer DOI-backed metadata when available. Never invent bibliographic fields.

If Zotero is connected, use it as the reference-management layer and preserve stable identifiers.

## Step 16 — Citation audit

Before finalizing, check:
- every important claim has support;
- citations point to the correct source;
- quoted text is exact and locatable;
- DOI/author/year/title metadata are consistent;
- primary and secondary sources are distinguished;
- uncertainty is visible;
- search limitations are disclosed;
- no database search is claimed without actual access;
- references contain no invented entries;
- conclusions do not exceed the evidence.

Write the result to `audit.md`.

## Step 17 — Final quality gate

A project is complete only when:

`Question defined + Search logged + Sources deduplicated + Screening documented + Evidence extracted + Literature synthesized + Gap assessed + Analysis justified + Citations audited + Limitations disclosed`

If one element is missing, report it explicitly instead of silently filling the gap.

## Output principle

The final deliverable should be a reproducible research package, not merely prose. The user should be able to inspect how the literature was found, why sources were included, what evidence supports each major conclusion, and how the final paper was produced.
