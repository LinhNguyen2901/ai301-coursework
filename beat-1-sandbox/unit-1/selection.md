# Unit 1 — Issue Selection

Path: `beat-1-sandbox/unit-1/selection.md`

Record of the issue carried into Unit 2, and of the evaluation runs that produced
`eval-run.txt`. This file is graded at the path above; a copy kept anywhere else in
the repository is not read.

Complete every labelled field below. Each is graded on its own; content placed under the
wrong label is not graded.

---

## Selected issue

**Issue link**

https://github.com/codepath/pathreview-ai301-fa26-s3/issues/26

**Verdict output**
```
All three issues pass every required check, so all three are accepted. For your fit profile, #26 is the best pick, then #63, then #47.

gh isn't installed here, so I collected the evidence from the public GitHub REST API. Figures below are as of 2026-09-29.

Repo-level checks (same for all three):
- maintainer_active: pass. The newest commit on main is from 2026-09-16, 13 days ago.
- repo_in_use: pass. The repo isn't archived and that commit is within 30 days. No merged PRs showed up, but the rubric only needs one of the two.
- policy_allows_ai: pass. docs/CONTRIBUTING.md and the PR template say nothing about AI. Silence passes.
- contributing_docs (preferred): pass. docs/CONTRIBUTING.md and docs/SETUP.md both exist.

Ranked (accepted, in fit order):
1. #26: add a safety event count to /health. This is Python backend work. It connects an API route (api/routes/health.py) to a service method (SafetyMonitor.get_event_count()), the kind of API and data-handling work your fit profile asks for.
2. #63: README scorer test fixture too short. It's Python test tooling with an exact repro (assert 51 > 100). Very well scoped, but it only touches a fixture, not backend logic.
3. #47: add curl examples to docs/API.md. It's API-related but docs-only, with no code logic, so it's the weakest fit.

The preferred-check scores are tied at 3 of 4 for all three, and none has a maintainer comment to break the tie, so fit alone decides the order.

Rejected: none.

Things to be aware of:
- Each issue already has a classmate's claim and repro comments: Alonso-Lopez-1 on #63, jeff-sp on #47, AdamLewis73 on #26. The Path Review house rule says those don't block you, so not_already_claimed passes on the other two conditions: no assignee, and no open or closed PR mentions any of the three.
- maintainer_endorsed fails on all three. A collaborator opened each issue, but no maintainer has commented in the threads.
- For #26 and #63, CONTRIBUTING says planted bugs have strict=True xfail tests. Your PR must remove the @pytest.mark.xfail marker, or CI fails.

[
  {
    "item": "https://github.com/codepath/pathreview-ai301-fa26-s3/issues/26",
    "checks": [
      {"name": "maintainer_active", "grade": "pass", "evidence": "Newest main commit 2026-09-16 (Andrew Burke), 13 days before 2026-09-29"},
      {"name": "repo_in_use", "grade": "pass", "evidence": "archived: false; newest main commit 2026-09-16 is within 30 days"},
      {"name": "scope_fits_newcomer", "grade": "pass", "evidence": "Concrete bug: /health returns literal 0 for safety_events_last_hour; files api/routes/health.py, safety/monitoring.py; no epic/RFC label, not blocked"},
      {"name": "not_already_claimed", "grade": "pass", "evidence": "No assignees; no PR references #26; AdamLewis73's 2026-09-25 claim is a classmate claim, which the Path Review house rule says to ignore"},
      {"name": "policy_allows_ai", "grade": "pass", "evidence": "docs/CONTRIBUTING.md and PR template contain no AI prohibition"},
      {"name": "newcomer_label", "grade": "pass", "evidence": "Labels: bug, good first issue, safety, tier-1"},
      {"name": "maintainer_endorsed", "grade": "fail", "evidence": "Only comments are from AdamLewis73 (association NONE); no maintainer comment"},
      {"name": "contributing_docs", "grade": "pass", "evidence": "docs/CONTRIBUTING.md and docs/SETUP.md exist"},
      {"name": "clear_acceptance", "grade": "pass", "evidence": "Before/after: field is literal 0 now; should reflect SafetyMonitor.get_event_count() counts"}
    ],
    "verdict": "accept"
  },
  {
    "item": "https://github.com/codepath/pathreview-ai301-fa26-s3/issues/63",
    "checks": [
      {"name": "maintainer_active", "grade": "pass", "evidence": "Newest main commit 2026-09-16, 13 days before 2026-09-29"},
      {"name": "repo_in_use", "grade": "pass", "evidence": "archived: false; newest main commit 2026-09-16 is within 30 days"},
      {"name": "scope_fits_newcomer", "grade": "pass", "evidence": "Concrete bug in test_readme_with_all_quality_signals: fixture has ~51 words vs assertion > 100; labels bug/tests, not blocked"},
      {"name": "not_already_claimed", "grade": "pass", "evidence": "No assignees; no PR references #63; Alonso-Lopez-1's 2026-09-24 claim is a classmate claim, which the house rule says to ignore"},
      {"name": "policy_allows_ai", "grade": "pass", "evidence": "docs/CONTRIBUTING.md and PR template contain no AI prohibition"},
      {"name": "newcomer_label", "grade": "pass", "evidence": "Labels: bug, good first issue, tests, tier-1"},
      {"name": "maintainer_endorsed", "grade": "fail", "evidence": "Only comments are from Alonso-Lopez-1 (association NONE)"},
      {"name": "contributing_docs", "grade": "pass", "evidence": "docs/CONTRIBUTING.md and docs/SETUP.md exist"},
      {"name": "clear_acceptance", "grade": "pass", "evidence": "Test to pass: `pytest tests/unit/test_readme_scorer.py -q`, currently fails with `assert 51 > 100`"}
    ],
    "verdict": "accept"
  },
  {
    "item": "https://github.com/codepath/pathreview-ai301-fa26-s3/issues/47",
    "checks": [
      {"name": "maintainer_active", "grade": "pass", "evidence": "Newest main commit 2026-09-16, 13 days before 2026-09-29"},
      {"name": "repo_in_use", "grade": "pass", "evidence": "archived: false; newest main commit 2026-09-16 is within 30 days"},
      {"name": "scope_fits_newcomer", "grade": "pass", "evidence": "Specific change to a named file: add example curl invocations to docs/API.md; labels good first issue/docs, not blocked"},
      {"name": "not_already_claimed", "grade": "pass", "evidence": "No assignees; no PR references #47; jeff-sp's 2026-09-27 claim is a classmate claim, which the house rule says to ignore"},
      {"name": "policy_allows_ai", "grade": "pass", "evidence": "docs/CONTRIBUTING.md and PR template contain no AI prohibition"},
      {"name": "newcomer_label", "grade": "pass", "evidence": "Labels: good first issue, docs, tier-1"},
      {"name": "maintainer_endorsed", "grade": "fail", "evidence": "Only comments are from jeff-sp (association NONE)"},
      {"name": "contributing_docs", "grade": "pass", "evidence": "docs/CONTRIBUTING.md and docs/SETUP.md exist"},
      {"name": "clear_acceptance", "grade": "pass", "evidence": "Before/after: docs/API.md has no example invocations; done when endpoints have curl examples"}
    ],
    "verdict": "accept"
  }
]

✻ Worked for 5m 14s · done 9:09 PM
```

---

## Eval iterations

**Run history**

First full run: 14/20 agreement, category floor unmet in `policy` (0/1). Failures
traced to `maintainer_active` requiring a maintainer comment within 30 days, which
was too strict — several healthy repos had long individual response times despite
recent commits. Also missing any check for contribution-policy language banning
AI-assisted contributions, which caused a false accept on issue-12.

Revised `maintainer_active` to rely on recent default-branch commit activity rather
than a hard maintainer-comment window, and added `policy_allows_ai` to check the
CONTRIBUTING.md AI-use section. Re-ran the affected issues with `--only`, then ran
the full eval again: 18/20 agreement, all categories at or above their floor. Two
remaining misses (issue-15, issue-20) were both false accepts, traced to missing
checks for repeated failed-claim history and non-human (bot) issue authors. Added
`no_failed_attempts` and `human_reported` to address these, re-ran the affected
issues, then ran the full eval a final time: 18/20 agreement, `run written to
eval-run.txt`.

Later, live mode on the Path Review repo rejected every candidate issue on
`repo_in_use`, because the repo had 0 merged PRs (freshly seeded, no student PRs
merged yet). Loosened `repo_in_use` to also pass on recent default-branch commit
activity, not just merge history, and re-ran the full eval to confirm the change:
18/20 agreement, `run written to eval-run.txt`.

**Issue analysis**

issue-12 (bookwyrm-social/bookwyrm#1133). Gold label: reject. My rubric's first
version graded this issue accept, because on the surface it looked healthy —
recent commits, decent maintainer response sample, and a "good first issue" label.
What my rubric missed was the repo's contribution policy, which states in
CONTRIBUTING.md: "We do not accept AI-generated code or documentation." That's an
explicit block on the kind of AI-assisted contribution this tool is meant to
support, and nothing in my original checks read that field at all. I added a
`policy_allows_ai` check that reads the contribution-policy text directly and
fails when it explicitly prohibits AI contributions, which correctly rejects this
issue.

**Check rationale**

`policy_allows_ai`: "The contribution policy does not explicitly prohibit
AI-generated code, documentation, or contributions." I worded it this way because
the evidence available to the grader is the literal CONTRIBUTING.md text, not an
inference about the maintainers' general attitude. A repo that says nothing about
AI should pass (silence is not a ban), while a repo that states a clear
prohibition, like bookwyrm's, should fail regardless of how active or well-run the
project otherwise looks. Making it a required check means no amount of activity or
scope quality can outweigh an explicit policy block.

**Trade-offs**

`repo_in_use` originally required a merged PR within the last 60 days, which is a
reliable signal on established open-source repos but fails on a freshly-seeded
classroom repo like Path Review, where no student PR has been merged yet. I loosened
it to also pass on recent default-branch commit activity, so the check no longer
rejects every issue in a new repo. The trade-off is that this version can no longer
tell the difference between a repo that is genuinely active and one where a
maintainer pushed a small commit but isn't actually reviewing or merging
contributions — a repo could pass `repo_in_use` on commit recency alone while still
being effectively unresponsive to PRs. I accepted that gap because, without it, the
check would have rejected every candidate in the one repo this tool is actually used
against in live mode.

---

## Selection rationale

**Selection rationale**

1. I want to focus on backend work in Python, Java, C++, or Go, and avoid frontend.
   Issue #26 is a Python backend bug in `api/routes/health.py` and
   `safety/monitoring.py`, so it matches both my language and my backend preference
   directly. It's also small enough to fit the time I have available for a first
   contribution.

2. The verdict correctly identified that the issue has a concrete before/after
   condition (the `/health` endpoint always reports 0 instead of the real count
   from `SafetyMonitor.get_event_count()`), that it isn't blocked or already
   claimed by policy, and that the repo's contribution policy doesn't prohibit
   AI-assisted work. What the rubric couldn't weigh is fit: it doesn't know that
   this issue touches the specific kind of API/service code I want more practice
   with, compared to #63 (test-only) or #47 (docs-only), which were accepted but
   ranked lower for that reason.

3. I expect the main difficulty to be smaller than it looks: the fix is localized
   to two named files, and the bug is already precisely described (literal 0 vs.
   the real counter value). The main friction will likely be around the
   `@pytest.mark.xfail(strict=True)` marker noted for planted bugs in this repo —
   I'll need to remove it as part of the fix or CI will fail, which is an
   easy-to-miss step for a first-time contributor.