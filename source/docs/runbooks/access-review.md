# Run a periodic access review

Access permissions accumulate over time. People join, change roles, and leave. Accounts go undeprovisioned. Service integrations are set up for a project and forgotten. The result is an environment where a significant proportion of active credentials belong to people who no longer need them, or grant more permission than anyone can justify.

An access review makes the current state visible and leaves a record of deliberate decisions about who has access to what, and why.

Run it quarterly for cloud and SaaS systems, and on every staff departure or role change.

## Define scope

List every system that holds data or provides access to other systems:
- Cloud platforms (AWS, GCP, Azure)
- SaaS applications (email, HR, CRM, project management, finance tools)
- Code repositories
- Internal infrastructure (VPN, admin panels, databases)
- Third-party integrations (anything with API keys or OAuth connections)

An incomplete list is not a blocker; building one is itself a useful output of the first review.

## Export current user lists

For each system, pull the list of active accounts. Most SaaS tools have an admin view; cloud platforms have IAM consoles. Capture username, email, role or permission level, last active date where available, and whether the account belongs to a person or is a service account.

## Compare against current staff

Cross-reference the account list against the current HR or staff record. Flag:
- Accounts belonging to people who have left.
- Accounts belonging to people who changed roles but kept old permissions.
- Service accounts with no identified owner.
- Accounts inactive for more than 90 days.

## Review permissions

For the remaining accounts, check whether the permission level matches the current role. Common findings:
- Admin access granted temporarily and never revoked.
- Broad read permissions on systems an individual no longer works with.
- Shared accounts or credentials, worth eliminating and replacing with individual accounts.

Apply least privilege: the minimum access needed to do the job, not the maximum that is convenient to grant.

## Deprovision and adjust

For each flagged account, deprovision if the person has left, adjust permissions if the role has changed, and assign an owner to any unowned service account or deprovision it.

For sensitive actions, such as removing admin access from an active user, confirm with their manager first and document the confirmation.

## Document

Record what was reviewed, what was found, and what was done, with a date. This creates accountability for the decisions and a baseline for the next review.

Keep this documentation somewhere reachable during an incident, not only in a system that the people who need it may be locked out of.

## Automate what is feasible

Where systems support it, automatic deprovisioning on HR-record closure is worth configuring. Even an imperfect automation that catches 70% of leavers promptly beats a manual process that catches all of them eventually. Most identity providers (Okta, Azure AD, Google Workspace) support SCIM provisioning that can automate this where the SaaS applications support the protocol.
