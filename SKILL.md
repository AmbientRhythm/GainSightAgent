---
name: Gainsight Customer Account Insight
description: Use this skill when a Customer Success Manager asks about a customer or account. Query Gainsight first and base the response on the returned data.
parameters:
  - name: customer_name
    type: string
    required: true
    description: Customer or account name to look up in Gainsight.
  - name: account_id
    type: string
    required: false
    description: Gainsight account identifier, if available.
  - name: customer_id
    type: string
    required: false
    description: Gainsight customer identifier, if available.
  - name: time_window
    type: string
    required: false
    description: Optional date range for recent activity or health changes.
  - name: region_or_segment
    type: string
    required: false
    description: Optional region, segment, or business unit filter.
---

# Gainsight Customer Account Insight

Use this skill when a Customer Success Manager asks about a customer or account.

## Instructions
- Query Gainsight before answering any question about a customer or account.
- Base the response only on data returned from Gainsight.
- Do not rely on assumptions, memory, or general knowledge when customer/account data is available.
- If required data is missing, say so clearly and do not guess.

## Behavior
When a CSM asks about a customer or account, query Gainsight first and base the answer on the returned data.

Summarize the customer/account concisely and highlight:
- Key customer health signals
- Risks or concerns
- Recent changes or notable activity
- Recommended areas for CSM attention

## Response format
Return a brief summary with the following structure:
1. Customer/account overview
2. Key health signals
3. Risks or concerns
4. Recent changes or notable activity
5. Recommended CSM focus areas
6. Data confidence note, if relevant

## Guardrails
- Keep the response concise and business-friendly.
- Prioritize facts from Gainsight over commentary.
- Highlight only material health signals and actionable follow-ups.
- If data is partial, stale, or incomplete, explicitly mention the limitation.
