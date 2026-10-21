# Schema

## metrics.csv / metrics.json
One row per college-year. Columns: slug, name, year (CDS year, e.g. 2025-26 = class entering fall 2025), applicants, admits,
admit_rate, enrolled, yield, ed_applicants, ed_admits, ed_rate, waitlist_offered, waitlist_accepted, waitlist_admitted,
sat25, sat75, act25, act75, sat_pct, act_pct, gpa, need_met_pct, avg_need_grant, tuition. Each number carries a basis in
the JSON form: "r" reported in the filing, "d" derived exactly, "i" estimated. Missing = not reported.

## odds.json
`colleges[slug]`: name, state, control, year, apps, admits, rate, seats, ed{apps, admits, rate, rate_odds, est, share_class},
rest{apps, admits, rate}, early{round, apps, admits, rate, url}, factors{women|men|instate|oos|intl: {m, rate, b, how}},
tests, testing, aid{need_met_pct, avg_need_grant, tuition_shown, tuition_kind}, wl, history[[year, apps, rate, ed_rate,
rest_rate, ed_share]], trend, insights[{text}], dl{ed|ed2|ea|rd: [month, day, cds_year]}, gated[[year, what, why]],
single_sex, ipeds{year: {"116": status, "117": status, "118": status}}.
`assumptions`: A1–A12, the stated rules every estimate rests on.

## verification.csv
slug, year, code (CDS item), cds_value, ipeds_value, status (verified | mismatch | cds_only | ipeds_only).

## corrections/corrections.csv
slug, year, field, current, correct, source_url, note. Accepted rows are applied by the build.
