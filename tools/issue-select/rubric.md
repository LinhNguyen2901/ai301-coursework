# Rubric: is this a good first issue?

## Checks

| Check | Evidence | Pass condition | Weight |
|---|---|---|---|
| maintainer_active | Repo-facts block: last default-branch commit date; maintainer first-response sample | Newest default-branch commit is within 90 days of today. Maintainer response sample is informational only and does not by itself fail this check | required |
| repo_in_use | Repo-facts block: archived flag, most recent merged PR date, most recent default-branch commit date | Repo is not archived AND (at least 1 PR was merged in the last 60 days OR the newest default-branch commit is within 30 days of today) | required |
| scope_fits_newcomer | Issue title, body, and labels | The issue names a concrete deliverable (a bug with its symptom, a specific change, or specific pages/files/functions to write or edit) AND is not labeled epic/RFC/discussion/design AND the body does not say it is blocked on an unmerged PR or an undecided design | required |
| not_already_claimed | Issue assignee field; issue comment thread; linked/cross-referenced PRs | No assignee, AND no comment in the last 30 days saying someone is working on it or asking to be assigned without a maintainer decline, AND no open PR that references the issue | required |
| newcomer_label | Issue labels | Has "good first issue" or "help wanted" | preferred |
| maintainer_endorsed | Comment thread on the issue | A maintainer commented on this issue itself, confirming it is valid or welcome | preferred |
| contributing_docs | Repo file list from repo-facts or evidence-guide | CONTRIBUTING file or a README setup section exists | preferred |
| clear_acceptance | Issue body | States a concrete done condition (expected output, test to pass, or before/after behavior) | preferred |
| policy_allows_ai | Repo-facts block: contribution policy text (CONTRIBUTING.md section) | The contribution policy does not explicitly prohibit AI-generated code, documentation, or contributions | required |

## Verdict rule

Accept if every required check passes. Reject if any required check fails.
`unclear` on a required check counts as fail. Preferred checks never change
the verdict; they only rank accepted issues (more preferred passes ranks
higher, ties broken by the newest maintainer activity).