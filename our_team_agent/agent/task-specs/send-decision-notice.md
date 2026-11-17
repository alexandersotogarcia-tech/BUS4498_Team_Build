# T05 Send Decision Notice

**Automation level:** L2 (AI-assisted, human-approved)

**Purpose:** Tell the requester the decision and reasons in a clear message.

**Inputs and sources:** Advisor decision and reasons (T04); requester email from the request record.

**Outputs and recipients:** One email to the requester, copy to the advisor.

**Tool:** Draft Decision Email (type: LLM text generation; permission: write drafts only). The advisor reviews the draft and clicks send.

**Limits:** Timeout 60 seconds. Retry up to 2 times, then use the plain-text template.

**Success check:** Requester receives the email and the request record is marked "closed".
