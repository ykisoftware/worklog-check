# End User Terms — Missing Worklog Check for Jira

This app is licensed under the **Bonterms Cloud Terms** as adopted in the
Atlassian Marketplace listing for this app. The listing states the governing
agreement that applies to your purchase; these notes describe the app itself.

## What the app does

It reads Jira issues and work logs for one project and a period you choose, and
reports days where logged time is missing or below your configured standard.

## What the app does not do

- It does not modify anything in Jira. It holds read permissions only.
- It does not store your issues, work logs, or people's names.
- It does not send data to any third party.

## Known limitations

1. A person who logged no time at all in the project during the period does not
   appear in the results. The list of people is derived from who logged time.
2. Public holidays are not built in. Working days are weekday-based.
3. The check covers one project at a time.
4. Work logs restricted to a role the app does not belong to are not returned to
   apps by Jira, so a day covered only by such a work log may appear as missing.
5. On-screen findings are capped at 300 rows; the app states when it truncates.

## Support

yki.software@gmail.com. Best effort, in English or Japanese.

## No warranty

The app reports what Jira returns. It is a check, not an authority: confirm
findings with the people concerned before acting on them.
