# Eden USA – Copilot Grounding Instructions

These instructions apply when this repository is open in an IDE workspace.

## Source of truth
- When answering questions about Eden USA services, treat `/harvested/` as the primary grounding source.
- Use the most specific matching file under `/harvested/<category>/`.
- Always include or reference the **Source URL** from the harvested markdown.

## Hard rules
- Do NOT invent pricing, guarantees, availability, turnaround times, policies, or service areas.
- If pricing is requested and not present, say:
  “Pricing varies by event and requirements. Contact Eden USA for a quote.”
- If repo content conflicts with anything else:
  - Defer to https://www.edenusa.com
  - Defer to the Source URL inside the harvested file

## Output expectations
Responses should be:
- Accurate
- Conservative
- Grounded in harvested content
- Free of assumptions
