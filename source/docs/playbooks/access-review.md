# Run a periodic access review

Access permissions accumulate over time. People join, change roles, and leave. Accounts
are not deprovisioned. Service integrations are set up for a project and forgotten. The
result is an environment where a significant proportion of active credentials belong to
people who should no longer have them, or grant more permission than anyone can justify.

An access review makes the current state visible and creates a record of deliberate decisions
about who should have access to what.

Run this quarterly for cloud and SaaS systems, and on every staff departure or role change.

## Define scope

List every system that holds data or provides access to other systems:
- Cloud platforms (AWS, GCP, Azure)
- SaaS applications (email, HR, CRM, project management, finance tools)
- Code repositories
- Internal infrastructure (VPN, admin panels, databases)
- Third-party integrations (anything with API keys or OAuth connections)

If you do not have a complete list, building one is itself a useful output of the first review.

## Export current user lists

For each system, pull the list of active accounts. Most SaaS tools have an admin view; cloud
platforms have IAM consoles. Capture: username, email, role/permission level, last active date
(where available), and whether they are a direct account or a service account.

## Compare against current staff

Cross-reference the account list against your current HR or staff record. Flag:
- Accounts belonging to people who have left.
- Accounts belonging to people who have changed roles and whose permissions have not been updated.
- Service accounts with no identified owner.
- Accounts that have not been active for more than 90 days.

## Review permissions

For remaining accounts, check whether the permission level matches the current role. Common
findings:
- Admin access granted temporarily that was never revoked.
- Broad read permissions on systems an individual no longer works with.
- Shared accounts or credentials (these should be eliminated and replaced with individual accounts).

Apply the principle of least privilege: the minimum access required to do the job, not the maximum
that is convenient to grant.

## Deprovision and adjust

For each flagged account: deprovision if the person has left, adjust permissions if the role
has changed, assign an owner to any unowned service account or deprovision it.

For sensitive actions (removing admin access from an active user), confirm with their manager
before acting, and document the confirmation.

## Document

Record what was reviewed, what was found, and what was done. Date the record. This serves
two purposes: it creates accountability for the decisions made, and it provides a baseline
for the next review so you can track whether the environment is improving.

Do not file this documentation only in a system that the people who need it cannot access
during an incident.

## Automate what you can

If your systems support it, configure automatic deprovisioning on HR record closure. Even
an imperfect automation that catches 70% of leavers promptly is better than a manual process
that catches all of them eventually.

Most identity providers (Okta, Azure AD, Google Workspace) support SCIM provisioning that
can automate this if your SaaS applications support the protocol.
