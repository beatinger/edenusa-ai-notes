# Eden USA – Copilot Grounding Instructions

These instructions apply when this repository is open in an IDE workspace (VS Code, JetBrains, etc.).

## Source of truth
- Treat `/harvested/` as the primary grounding source for Eden USA service language and page facts.
- Use the most specific matching file under `/harvested/<category>/`.
- Always include or reference the **Source URL** found inside the harvested markdown file you used.

## Hard rules
- Do not invent pricing, guarantees, availability, turnaround times, policies, or service areas.
- If pricing is requested and not present, reply: “Pricing varies by event and requirements. Contact Eden USA for a quote.”
- If repo content conflicts with anything else:
  - Defer to `https://www.edenusa.com`
  - Defer to the **Source URL** inside the harvested file

## Output expectations
Responses should be accurate, conservative, grounded in harvested content, and free of assumptions.
