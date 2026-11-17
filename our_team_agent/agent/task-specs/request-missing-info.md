# T06 Request Missing Info

**Automation level:** L1 (rule-based automation)

**Purpose:** Ask the requester for the missing fields so the request can be rechecked.

**Inputs and sources:** Missing-field list from T02; requester email from the request record.

**Outputs and recipients:** A templated email to the requester. When the requester resubmits, the request returns to T02.

**Tool:** Send Missing Info Email (type: email send; permission: send from the club-requests address, templates only)

**Limits:** Timeout 30 seconds. Retry up to 2 times, then alert the advisor. Remind after 3 days; close the request after 10 days with no reply.

**Success check:** Email sent and the request marked "waiting on requester".
