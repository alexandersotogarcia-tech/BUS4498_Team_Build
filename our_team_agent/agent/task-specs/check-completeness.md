# T02 Check Completeness

**Automation level:** L1 (rule-based automation)

**Purpose:** Confirm every required field is filled before review.

**Inputs and sources:** Request record from the Requests Sheet (T01), or a resubmission (T06).

**Outputs and recipients:** Status "complete" or "incomplete" plus a list of missing fields. Complete goes to T03; incomplete goes to T06.

**Tool:** Validate Required Fields (type: script rule check; permission: read the sheet, write the status column)

**Limits:** Timeout 30 seconds. Retry up to 2 times, then route to the advisor manually.

**Success check:** Every record has a status and, if incomplete, a missing-field list.
