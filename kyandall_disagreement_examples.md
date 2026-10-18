# MiniProject3 Disagreement Examples (kyandall)

**Parties:** Keoni Yandall (`kyandall`) and teammate `jbronyah`. Each disagreement was settled by comparing the evidence each of us recorded against the projects' commit histories. Examples 1 and 2 come from `kyandall_validation_log.csv` (kyandall validating jbronyah). Examples 3 and 4 come from `jbronyah_validation_log.csv` (jbronyah validating kyandall).

## Example 1: `ericproffitt_topicmodelsvb.jl`, WhyRecovered

- **Author (jbronyah):** "Maintenance updates, bug fixes, or compatibility adjustments"
- **Validator (kyandall):** "Recovery cause not established from summary"
- **Why we differed:** The author applied one generic category to every project that had a gap. The validator wanted a specific post-gap commit, issue or PR before naming a cause.
- **Evidence discussed:** Longest gap of 23 months, from 2023-03 to 2025-01. The only commits after it are `fae1bd7` and `a91ae62`, both "Update README.md" on 2025-02-09. No code changes, bug fixes or dependency changes follow the gap.
- **Resolution:** ValidatorKept. Adjudicated value: "Recovery cause not established from summary".
- **Justification:** Two README edits can't support a claim of bug fixes or compatibility work. Without a stated reason in the history, the more cautious wording is the one the evidence supports.

## Example 2: `hbctraining_scrna-seq_online`, WhyRecovered

- **Author (jbronyah):** "Maintenance updates, bug fixes, or compatibility adjustments"
- **Validator (kyandall):** "Recovery cause not established from summary"
- **Why we differed:** The author treated the 14-month interval (2018-02 to 2019-03) as a recovery episode. The validator questioned what the post-gap work actually was.
- **Evidence discussed:** The only commit before the interval is `1e2bd66`, dated 2017-12-31. The work after it opens with `0565183` "Initial commit" and `502ce35` "added all materials for scRNA-seq workshop from long course", both on 2019-04-09. The "gap" is pre-launch history, not a decline followed by a recovery.
- **Resolution:** ValidatorKept. Adjudicated value: "Recovery cause not established from summary".
- **Justification:** Creating the repository isn't maintenance, so the generic category misdescribes it. HasRecovered stays Yes, because the project's later 3-month gaps (2019-08 to 10, 2023-03 to 05, 2024-03 to 05) were each followed by resumed work.

## Example 3: `https://github.com/ANTsX/ANTsR`, ActivityPattern

- **Author (kyandall):** irregular
- **Validator (jbronyah):** declining
- **Why we differed:** The author focused on the uneven month-to-month bursts. The validator focused on the long-run trend.
- **Evidence discussed:** Annual commits fell from 1,565 (2015) to 455 (2017), 146 (2019), 24 (2021) and 30 (2023). They rebounded to 251 in 2024 but stayed far below the peak.
- **Resolution:** ValidatorKept. Adjudicated value: declining.
- **Justification:** "Irregular" fits a series with no trend. ANTsR has a clear, sustained downward trend, and its partial rebound doesn't reverse it. We used the same rule for other projects with a peak and a partial rebound.

## Example 4: `https://github.com/WorldWideTelescope/wwt-web-client`, RecentThemes

- **Author (kyandall):** Automated bot contributions:Other
- **Validator (jbronyah):** Other:Bug fixes
- **Why we differed:** We sampled different commits. The author used the all-branch export from MiniProject2. The validator took the latest 10 default-branch commits through 2025-09-30.
- **Evidence discussed:** The validator's sample has 6 CI, deployment or contact-info commits (Other) and 4 viewport or place-sharing fixes (Bug fixes). The Cranko-generated release commits behind the author's bot label appear in the all-branch export but not in the default-branch sample.
- **Resolution:** AuthorKept. Adjudicated value: Automated bot contributions:Other.
- **Justification:** Both labels are accurate for the sample they came from, so the disagreement is about method rather than coding. We kept the author's label because it came from the MiniProject2 dataset, which defines the commit population being validated.
