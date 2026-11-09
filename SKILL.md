---
name: se-legal-mcp-skill
description: Official Sweden (SE) legislation, multi-tier court precedent research, and citation verification skill.
version: 2.0.0
author: JurisAtlas
license: MIT
---

# Sweden Legal Research & Multi-Tier Case Law Skill (`se-legal-mcp`)

Use this skill whenever the user asks a legal question, drafts a pleading or contract, or researches case law across any judicial instance in **Sweden (SE)**.

## Verification & Research Rules

1. **Citation Verification:** Never fabricate a statutory provision or case citation. Query `search_legislation`, `search_case_law`, `search_tiered_court_decisions`, or `verify_citation` before citing any authority (e.g., `NJA 2024 s. 10 or SFS 2024:12`).
2. **Multi-Tier Judicial Coverage:**
   - **First Instance (Trial / Municipal / District):** 48 Tingsrätter (District Courts), 12 Förvaltningsrätter (Administrative Courts) & Mark- och miljödomstolar
   - **Second Instance (Cantonal / Regional / Appellate):** 6 Hovrätter (Svea, Göta, Skåne och Blekinge, Västra Sverige, Nedre Norrland, Övre Norrland) & 4 Kammarrätter (Stockholm, Göteborg, Sundsvall, Jönköping)
   - **Supreme & Constitutional Instance:** Högsta domstolen (HD), Högsta förvaltningsdomstolen (HFD), Arbetsdomstolen & Mark- och miljööverdomstolen
   - **Primary Tiered Database:** Domstolsverket Vägledande avgöranden (rattspraxis.etjanst.domstol.se — HD, HFD, Hovrätter & Kammarrätter) (`https://rattspraxis.etjanst.domstol.se`)
