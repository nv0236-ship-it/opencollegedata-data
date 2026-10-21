# Open College Data

Every college's own admissions numbers (the Common Data Set it files each year), checked against federal IPEDS data,
for 320 US colleges and about 2,200 college-years. Free under CC BY 4.0. Site: https://opencollegedata.org

This repo is the published data, its schema, and the place to correct it.

## Files
- `data/colleges-index.json` — name (and common short names) → slug
- `data/metrics.json`, `data/metrics.csv` — one row per college-year: applicants, admits, admit rate, enrolled, yield,
  Early Decision, waitlist, test ranges, aid
- `data/odds.json` — per college, latest year: everything the odds model rests on, each value with its basis
  (r reported, d worked out, i estimate), trends, deadlines, the numbered assumptions. Third-party rankings and student
  posts are not included.
- `data/verification.csv` — each checked number against IPEDS, with its status
- `data/insights.json` — cross-college findings
- `data/openapi.json` — the free API (static files, CORS open, no key): https://opencollegedata.org/developers/
- `corrections/corrections.csv` — accepted corrections, applied at the next build

## Correct us
Open an issue (templates provided) or a pull request adding a row to `corrections/corrections.csv`:
`slug,year,field,current,correct,source_url,note`. Say where the right number is (the filing, IPEDS, a college page).
We acknowledge within 2 business days and ship accepted fixes with the next build; the issue is closed with a link.

## Licence and credit
Data: CC BY 4.0 — use it anywhere, credit "Open College Data (opencollegedata.org)". Source filings belong to the
colleges; federal data is public domain. Rankings belong to their publishers and are not in this repo.

## Disclaimer and independence
Numbers are read from the colleges' filings by software and by language model, checked against IPEDS, labelled by
method and status, and corrected when reported. They can still be wrong or filed differently by the college: check the
original filing (linked from every page on the site) before relying on a number. The data is provided as is, without
warranty. Open College Data is independent: not affiliated with, sponsored by or endorsed by any college, the Common
Data Set Initiative, the U.S. Department of Education or any ranking publisher. Rankings appear only per college, with
credit; student posts are not in this repository.

Requests to remove or change content: [TAKEDOWN.md](TAKEDOWN.md). Security: [SECURITY.md](SECURITY.md).
Terms: https://opencollegedata.org/terms/ · Sources: https://opencollegedata.org/sources/
