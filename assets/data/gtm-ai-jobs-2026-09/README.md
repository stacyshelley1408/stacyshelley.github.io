# How GTM job postings ask people to use AI (dataset, September 2026)

Stacy Shelley, stacyshelley.com. Boards fetched 24 to 26 September 2026.

Hand-coded dataset behind the study *What 3,821 job postings say about how GTM teams are told to use AI*. It records
not whether a posting mentions AI, but how the job is asked to use it: not at all, as something to sell, as an
attitude, to do existing work faster, to build or redesign, or to govern what AI produces.

## Frame
- 352 technology companies with public job boards on Greenhouse, Lever or Ashby. Companies that build AI models were
  excluded, as were non-technology employers.
- Companies came from three sources, reported separately because they differ: a list of security vendors,
  established software companies found through Wikipedia and careers pages, and companies found by searching for
  open marketing roles (so marketing-hiring companies are over-represented in that group).
- Job families were assigned from titles and audited by hand. Marketing: product marketing, demand generation,
  brand/content, marketing leadership, marketing operations. Sales side: account executives and sales leaders,
  SDR/BDR, presales.
- 3,821 postings analyzed (1,003 marketing, 2,818 sales side), one per company and text.

## Files
| file | rows | what it is |
|---|---|---|
| `postings.csv` | 4,486 | every candidate posting at the 352 companies, analyzed or not, with the reason for any exclusion |
| `posting_sentences.csv` | 15,305 | every AI-related sentence in an analyzed posting, with its code |
| `corrections.csv` | 48 | codes changed after the audits, with the reason; already applied in the other files |
| `codebook.md` | | code definitions, posting-level measures, and the audit rules |

### postings.csv
`posting_id`, `company`, `segment`, `ats`, `title`, `side` (marketing / sales-side), `family`, `location`,
`last_updated`, `fetched` (the day that company's job board was downloaded), `url`, `text_chars` (length of the full posting), `in_analysis`, `exclusion_reason`,
`codes` (all codes in the posting), `role_usage`, `task_named`, `build_redesign`, `u5_kind`, `generate_with_ai`.
Measures are blank for postings not in the analysis.

### posting_sentences.csv
`posting_id`, `company`, `section_heading`, `sentence`, `codes`, `placement`, `u5_kind`, `label_round`,
`corrected_after_audit`. A sentence that appears in several postings (company boilerplate) appears once per posting.
Email addresses are replaced with `[email removed]`.

## What is not included
Full posting text. It belongs to the employers; every posting keeps its public URL, and every AI-related sentence the
analysis rests on is included verbatim. Posting URLs will stop working as roles close.

## How it was coded
AI was used to build the collection scripts and to code every AI-related sentence against the codebook, one sentence
at a time. The codebook came from an exploration sample of 165 postings and was frozen before any analyzed posting
was read.
Audits, in brief (the full report is on the study page):
- Title audits of random samples until misfiled titles fell to about 2 to 5%.
- Duplicate, stale, empty and non-English posting checks.
- A full re-read of every "build/redesign" and "content governance" posting. That audit failed at first (about 1 in 5
  single-sentence build codes were wrong) and was fixed through `corrections.csv`.
- Blind re-labels: 150 sentences for consistency (98% agreement) and 160 across labeling rounds (95%).
- A blind check of coding symmetry between marketing and sales sentences, which found a lean worth about 2
  points on the sales-vs-marketing gap. Quote that gap as "about 30 points".

## Limits
- Postings record what employers write into a job, not what people in the job actually do.
- No second rater checked the coding independently. The blind checks measure consistency, not independent agreement.
- One snapshot. No trends.
- Not a random sample of all technology companies; report rates by segment.

## License
The coding, derived fields and documentation are released under CC BY 4.0. Quoted posting sentences remain the
employers' text, included for research and commentary. Please cite as: Shelley, S. (2026). *How GTM job postings ask
people to use AI* [dataset]. stacyshelley.com.
