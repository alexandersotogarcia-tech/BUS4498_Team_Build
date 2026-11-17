# T03 Review Budget

**Automation level:** L3 (agent)

**Purpose:** Review the budget against club funding rules and write a short summary with flagged issues for the advisor.

**Inputs and sources:** Complete request record (T02); Club Funding Policy PDF (stored in the team folder).

**Outputs and recipients:** A review summary (total, allowed vs. disallowed items, flags, recommendation) sent to the advisor in T04.

**Tools (verb-object names):**

| Tool | Type | Permission | Timeout | Retry limit |
|---|---|---|---|---|
| Read Policy Document | file read | read-only | 30 s | 2 |
| Calculate Budget Total | calculator script | no external access | 10 s | 1 |
| Draft Review Summary | LLM text generation | write to the review column only | 60 s | 2 |

**Boundaries:** The agent may not approve or deny, send email, or edit the request itself. It must cite the policy section for every flag.

**Escalation:** If the budget is unreadable, totals do not match, or a tool fails after its retries, pass the request to the advisor marked "manual review needed".

**Success check:** Summary contains a total that matches the sum of the line items and a recommendation labeled "advisory only".
