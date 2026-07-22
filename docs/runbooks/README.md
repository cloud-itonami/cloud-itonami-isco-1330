# AI data-center operating runbooks

Every execution creates a ticket with asset IDs, operator, timestamps,
evidence and outcome. Physical/security-sensitive steps require an approved
change and two-person verification. Site emergency procedures and equipment
manufacturer instructions override these generic runbooks.

| Runbook | Trigger | Approval gate |
|---|---|---|
| `01-procure-to-rack.md` | approved purchase | PO, energisation, acceptance |
| `02-daily-operations.md` | scheduled | none for observation; change approval for action |
| `03-incident-response.md` | alert/report | containment that affects tenants |
| `04-change-maintenance.md` | planned change | change owner + rollback |
| `05-security-access.md` | access request/event | privileged/physical access |
| `06-billing-settlement.md` | period close | invoice/revenue distribution |
| `07-decommission.md` | approved retirement | shutdown, data destruction, disposal |
| `08-cross-border-procurement.md` | international route | export/import and shipment release |

Before production, replace every `[SITE-SPECIFIC]` field and conduct a tabletop
exercise plus witnessed commissioning rehearsal.
