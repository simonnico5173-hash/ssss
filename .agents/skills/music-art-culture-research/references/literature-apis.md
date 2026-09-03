# Literature API Research Guide

## Purpose

Use this reference when automatic scholarly discovery is requested. The APIs are discovery/metadata tools; they are not substitutes for reading the actual source.

## OpenAlex

Best for broad scholarly discovery, works, authors, institutions, concepts, topics, and citation relationships.

Typical workflow:
1. Search works by concept/title/author.
2. Capture DOI, title, authors, year, venue, abstract/inverted abstract when available, open-access status, and cited-by information.
3. Follow related works and citations for high-value papers.
4. Prefer DOI/publisher metadata for final bibliographic verification.

## Crossref

Best for DOI registration metadata and bibliographic normalization.

Typical workflow:
1. Search by title, author, DOI, or bibliographic fields.
2. Normalize DOI, title, authors, publication date, container title, publisher, and type.
3. Use Crossref to resolve or verify DOI metadata when records disagree.
4. Do not treat Crossref metadata alone as evidence for a paper's substantive claims.

## Semantic Scholar

Best for scholarly discovery, paper relationships, abstracts when available, authors, citations, references, and related papers.

Typical workflow:
1. Search papers by topic/title/author.
2. Capture paper identifiers, DOI when present, abstract, year, venue, citation/reference relationships, and related papers.
3. Use influential citations as leads, then inspect the underlying source.

## Google Scholar / JSTOR / library databases

Use when the current environment legitimately provides access. These are useful for discipline-specific coverage and locating books/articles that broad APIs may miss.

Do not claim comprehensive coverage unless the search protocol and access support that claim.

## DOI and metadata rules

- Prefer DOI as the stable identifier when available.
- Verify important metadata against the publisher or authoritative registry.
- Never invent a DOI.
- Keep alternate identifiers/URLs when they help retrieval.
- Distinguish article, book chapter, book, conference paper, dataset, review, and preprint.

## Search design

Run multiple query families rather than one query:
- exact concept;
- synonyms;
- historical terminology;
- object/person/work names;
- method terms;
- competing explanations;
- review/systematic-review terms.

Record queries and search dates for systematic/scoping projects.

## Evidence boundary

Metadata can establish that a work exists and help locate it. Abstracts can support only claims contained in the abstract. Precise claims, quotations, page references, methods, results, and nuanced interpretations should be verified against full text whenever possible.
