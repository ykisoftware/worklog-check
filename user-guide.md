# Missing Worklog Check for Jira — User guide

## 1. Install and open (2 minutes)

1. Install the app from the Atlassian Marketplace.
2. Open any Jira project, then open the **Missing Worklog Check** tab on the
   project page.
3. The check runs automatically for the current month.

You must be a **project administrator** of the project you open. The results
show who has not logged time, so the app does not show them to anyone else. If
the app cannot confirm your permission, it shows nothing rather than guessing.

## 2. Reading the result

The summary line gives four numbers for the selected period:

| Number | Meaning |
|---|---|
| Days with no entry | A working day where that person logged 0 hours |
| Thin days | A working day where the logged time is below your standard hours |
| Untracked active issues | An issue updated in the period with no work log in it |
| Recoverable hours | Standard hours for empty days + the shortfall on thin days |

The detail list is sorted newest date first, so the most recent gaps — the ones
people can still remember — come first.

## 3. Choosing a period

**This month** and **Last month** are one click. For anything else, set the two
dates directly.

Two rules apply to every period:

- **The future is never counted as missing.** If today is the 21st and you
  select the whole month, the check stops at the 21st.
- **Days before a person's first logged day are never counted as missing.** A
  person who started mid-period does not appear with false gaps at the start.

## 4. Settings

- **Standard hours per day** — used by both the empty-day and thin-day checks.
  Default 8.
- **Working days** — which weekdays count. Default Monday to Friday. A weekday
  you uncheck is never reported as missing.
- **Excluded people** — click *Exclude* next to anyone who should not be
  checked. The setting persists, so leavers and part-timers stay out next month.

Settings are per project.

## 5. Exporting

The export block is CSV text. Select it, copy it, and paste it into a
spreadsheet or an email. It contains the project, the period, the time of the
check, and one row per finding.

## 6. What the app can and cannot see

- It reads issues and work logs **live** from Jira each time you run a check.
- It **cannot change anything** — the app holds read permissions only.
- It stores your project settings (standard hours, working days, excluded
  account IDs). It does not store names, issues, or work logs.
- Work logs restricted to a role the app does not belong to are not returned to
  apps by Jira, so a day covered only by such a work log can appear as missing.
- People who have never logged time in the project during the period do not
  appear at all: the roster is derived from who logged time.
- Public holidays are not built in. Uncheck the weekday, or read those rows as
  expected.

## 7. Troubleshooting

**"Only project administrators can view this."**
You are not an administrator of this project, or Jira did not return the
permission. Ask a project administrator to open it.

**A day is reported as missing but time was logged.**
Check whether the work log has a visibility restriction. Apps cannot read
restricted work logs.

**A holiday shows as missing.**
Working days are weekday-based. Uncheck that weekday or ignore those rows.

**The list says it was truncated.**
More than 300 findings were produced. Narrow the period.
