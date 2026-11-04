# ML Platform Research Register

Shared quarterly register of foundational machine-learning papers maintained by
the ML Platform research group at Northvale Analytics.

This repository holds the open curation requests and the register of papers that
the group has already accepted, so that each quarter starts from a consistent
baseline instead of a blank sheet.

## Repository layout

| path | purpose |
| --- | --- |
| `requests/` | open and completed curation requests |
| `registry/curated_index.csv` | papers accepted in previous quarters |
| `registry/2026-Q4-curated.csv` | this quarter's published register |

## Workflow

1. Read the open request under `requests/`.
2. Resolve every requested title against the team paper index. The index is a
   candidate generator, not a title oracle: confirm an exact title match
   (case, punctuation and whitespace insensitive) before using any returned
   identifier.  If no returned title matches, resolve the paper through a
   general search and use the canonical arXiv identifier you find there.
3. Open the resolved paper and read the first page to capture the first
   author's affiliation exactly as it is printed.
4. Assign Track / License Review / Owner Team with the policy below.
5. Publish the completed register to the path named in the request and set the
   request status to `completed`.

## Policy

- `Track` is `Industry` when the first author's affiliation names a for-profit
  company or corporate lab (for example Google, Microsoft, Meta, Amazon, Apple,
  OpenAI, NVIDIA, DeepMind, IBM); otherwise it is `Academia`.
- `License Review` is `Required` for Industry papers and `Not required` for
  Academia papers.
- `Owner Team` is `Legal` for Industry papers and `Research` for Academia
  papers.

## Register schema

| column | meaning |
| --- | --- |
| Title | canonical paper title |
| ArXiv ID | bare arXiv identifier, no `arXiv:` prefix and no version suffix |
| First Author | first author's full name |
| Affiliation | first author's affiliation as printed on page 1 |
| Track | Industry or Academia |
| Year | arXiv publication (first submission) year |
| License Review | Required or Not required |
| Owner Team | Legal or Research |
| Source URL | arXiv abstract page URL |
