# Workflow of Tasks

**Charter:** [Team charter](../../README.md)

**Trigger:** A club officer submits the Event Request Form.

**Completion condition:** The requester receives an approval or denial notice with reasons.

## Description

The form submission is stored (T01) and checked for required fields (T02). Complete requests go to the budget review agent (T03), whose summary goes to the advisor for the decision (T04). The decision is sent to the requester (T05). If a request is incomplete, the requester is asked for the missing items (T06) and resubmits, which restarts T02. If T03 cannot read the budget or the advisor does not respond in time, the request goes to the advisor for manual handling.

## Diagram

```mermaid
flowchart TD
A([Form submitted]) --> T01[T01 Collect Request]
T01 --> T02[T02 Check Completeness]
T02 -->|Complete| T03[T03 Review Budget]
T02 -->|Incomplete| T06[T06 Request Missing Info]
T06 -->|Requester resubmits| T02
T03 -->|Review summary ready| T04[T04 Approve Request]
T03 -.->|Budget unreadable or tool fails| T04
T04 -->|Decision made| T05[T05 Send Decision Notice]
T04 -.->|No response in 2 business days| E1[Escalate to department chair]
E1 --> T04
T05 --> Z([Requester notified - done])
```
