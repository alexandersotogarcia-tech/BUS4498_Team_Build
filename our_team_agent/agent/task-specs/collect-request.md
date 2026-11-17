# T01 Collect Request

**Automation level:** L1 (rule-based automation)

**Purpose:** Store each submitted Event Request Form as one record.

**Inputs and sources:** Form fields (club name, event, date, budget lines, requester email) from the Event Request Form.

**Outputs and recipients:** A request record in the Requests Sheet, read by T02.

**Tool:** Save Request Record (type: spreadsheet write; permission: append rows only)

**Limits:** Timeout 30 seconds. Retry up to 2 times, then flag the row "failed" and email the advisor.

**Success check:** One new row exists with a unique request ID.
