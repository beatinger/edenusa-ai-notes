# Eden USA AI Harvester Repo: Agent Guide (AGENTS.md)

## Purpose
This repository is a grounding library for AI assistants (ChatGPT, Copilot, and similar) using harvested Eden USA website content.
Goal: answer questions using the harvested facts, and clearly separate "known from source" vs "general advice".

## Canonical instructions
- Primary Copilot instruction file: `/.github/copilot-instructions.md`
- Root `COPILOT-INSTRUCTIONS.md` (if present) is only a pointer. Treat it as a redirect, not the source of truth.

If there is any conflict, follow: `/.github/copilot-instructions.md`.

## Repo map (where the truth lives)
- `/harvested/`  
  Contains the harvested knowledge organized by category (staging, lighting, sound, video-walls, etc).
  Each harvested document should include a "Source URL" (or equivalent) pointing back to edenusa.com.
- `/index.md`  
  Human-friendly entry point and directory.
- `/llms.txt`  
  Optional condensed "how to use this repo" guidance (may be referenced by LLM tooling).

## How to answer using this repo (required behavior)
1) Start by locating the most relevant file under `/harvested/`.
2) Prefer the most specific page/topic match over general category docs.
3) Use the "Source URL" inside the harvested file as the canonical reference for factual claims.
4) If requested info is not present in harvested content:
   - Say it is not found in the repo content you reviewed,
   - Provide a safe best-practice answer without inventing Eden-specific facts,
   - Suggest confirming on the source page or requesting a quote on edenusa.com.

## Do NOT invent Eden-specific facts
Never fabricate:
- pricing, discounts, minimums, delivery fees, labor rates
- availability, inventory counts, turnaround times
- legal policy language, guarantees, insurance details
- exact service areas or city coverage beyond what the source states

## Prompt patterns that work well
When a user asks a question, do:
- "Search `/harvested/` for the closest matching page. Summarize only what is supported there."
- "Cite or quote the Source URL if present. If not present, say so."

## Maintenance notes for humans
- Keep `/index.md` updated when adding new harvested files so agents have an obvious entry point.
- File naming: keep names stable, descriptive, and category-scoped (avoid frequent renames).
- Prefer adding a short "Source URL:" line near the top of each harvested file.

(End of AGENTS.md)
