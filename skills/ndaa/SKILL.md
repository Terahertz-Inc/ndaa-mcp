---
name: ndaa
description: Look up FY2027 NDAA bill status, section text, House vs Senate diffs, or related news from ndaa.ai.
---

# NDAA.AI public tracker

Every tool named below comes from `https://mcp.ndaa.ai/mcp`. No API key.

## Steps

1. **Status** — `get_status` for the current bill overview.
2. **Search** — `search_sections` with a keyword (e.g. cyber).
3. **Compare** — `compare_house_senate` on a section id from search when the user wants diffs.
4. Prefer tool results over memorized bill text; the tracker updates.

## Rules

- Read-only public data. Cite section ids from the tools.
- Docs: https://ndaa.ai/mcp

## Done when

- Answers rest on a tool result and name the section or status used.

