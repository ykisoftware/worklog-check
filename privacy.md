# Privacy Policy — Missing Worklog Check for Jira

**Last updated:** 2026-08-23

## What this app reads

When a project administrator opens the app, it reads the following from your
Jira site through the Atlassian REST API, and only for the project being viewed:

- Issues in the project: key, summary, status, and last-updated date
- Work logs on those issues: author account ID, author display name, start date,
  and time spent
- Whether the person viewing the page administers the project

The app does **not** read work log comment text, issue descriptions, issue
comments, attachments, or custom fields.

## What this app stores

The app stores **one record per Jira project**, in Atlassian's own Forge hosted
storage:

- Standard hours per day
- Which weekdays count as working days
- The Atlassian account IDs that an administrator excluded from the check

Nothing else is stored. Issues, work logs, display names, and check results are
read live on each run and discarded when the request ends. The app keeps no
history of results.

Atlassian account IDs are stored only because an administrator chose to exclude
those people, and that choice has to persist to be useful. No name, email
address, or work log content is ever written to storage.

## Where data is stored

Inside Atlassian's Forge platform. The vendor operates no server, no database,
and no analytics of its own. Nothing is sent to any third party.

## Deletion

Uninstalling the app removes its Forge storage. There is no vendor-held copy to
request the deletion of.

## Permissions

| Permission | Why it is needed |
|---|---|
| `read:jira-work` | Read issues and their work logs |
| `read:jira-user` | Show the display name next to each finding |
| `storage:app` | Store the project's settings |

The app holds no write permission and cannot change anything in Jira.

## Who can see the results

Project administrators only. The check is enforced on the server for every
request, and when the permission cannot be confirmed the app shows nothing.

## Contact

yki.software@gmail.com
