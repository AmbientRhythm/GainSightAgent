---
name: Gainsight Customer Account Insight
description: Use this skill when a Customer Success Manager asks about a customer or account. Query Gainsight first and base the answer on the returned data.
---

# Gainsight Customer Account Insight

Use this skill when a Customer Success Manager asks about a customer or account and needs a concise, evidence-based summary.

## Instructions
- Query Gainsight before answering any question about a customer or account.
- Base the response only on the data returned from Gainsight.
- Do not rely on assumptions, memory, or general knowledge when customer/account data is available.
- If the required data is missing, say so clearly and avoid guessing.

## Parameters
- customer_name: Customer or account name
- account_id: Gainsight account identifier, if available
- customer_id: Customer identifier, if available
- time_window: Optional date range for recent activity or health changes
- region_or_segment: Optional filter for region, segment, or business unit

## Response requirements
Summarize the account concisely and highlight:
- Key customer health signals
- Risks or concerns
- Recent changes or notable activity
- Recommended areas for CSM attention

## Output format
Provide a brief summary in this structure:

1. Customer/account overview
2. Key health signals
3. Risks or concerns
4. Recent changes or notable activity
5. Recommended CSM focus areas
6. Data confidence note, if relevant

## Example response pattern
"Based on Gainsight data for [customer_name/account_id], the account shows [health signal]. Key risks include [risk]. Notable recent activity includes [activity]. Recommended CSM attention: [focus area 1], [focus area 2]."

## Guardrails
- Keep the response concise and business-friendly.
- Prioritize facts from Gainsight over commentary.
- Highlight only material health signals and actionable follow-ups.
- If data is partial or stale, explicitly mention that limitation.
