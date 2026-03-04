# Campaign Index
**Campaign**: The Thornhaven Shadow Crisis
**Last updated**: After Session 17 (Day 24)

---

## Current State

**In-game day**: 24
**Eden's level**: 3 (Divination Wizard)
**Last session**: 17 — The lich confirmed. The disc built. The council convenes today.
**Spreadsheet ID**: 139NjvmH7wJa2FIlEbCrvxEqMitHSsWmYPMGXXvUmiy8

**Top 3 active threads**:
1. Divine Council convenes Day 24 — King present, three reformist exarchs committed, Serath not yet arrived, Vahlen searching
2. The lich — confirmed, deteriorating, recruiting a successor, manufacturing the exarch schism for centuries
3. The name under everything — Blackwater's folder, chain of recommendations going back centuries, working theory: the lich's infrastructure

**Next session hook**: The council opens. Portent is 2 and 7 — two forced failures, held. Which two things. When.

---

## File Directory

*One-line descriptions. Load the file; don't rely on the description.*

### Canonical Summaries
| File | Contents |
|------|----------|
| `SESSIONS_1-4_CANONICAL_SUMMARY.md` | Thornhaven crisis through royal court arrival. The grimoires, the cult, the father reunion. |
| `SESSIONS_5-17_CANONICAL_SUMMARY.md` | Royal court through Day 24. The full arc. Start here for any session 5+. |

### Reference Documents
| File | Contents |
|------|----------|
| `ENTITY_INDEX.md` | All significant entities with status tiers, source files, and cross-references. The retrieval layer. |
| `eden_sagebough_character_sheet.md` | Full character sheet including spells, items, income, psychology, session history summary. |
| `relationship_timeline_analysis.md` | Character-by-character relationship analysis, Day 9–17. Lyren, Kethris, Aldrin, Brecht, Celeste, Vahlen, Marta, mercenaries. |
| `SESSION_10_QUICK_START.md` | Best quick-start template if a faster load is needed. Treat as a format reference, not current state. |

### Session Summaries (complete record)
`session_1` through `session_17` — individual session files. Detailed scene-level record. Consult for specific moments, quotes, and tactical details not captured in the canonical summaries.

Notable individual files:
- `session_9_summary.md` — pocket realm extraction, full combat record
- `session_12_summary.md` — the insurrection, full combat record, casualties
- `session_13_summary.md` + `session_13_part2_summary.md` — funerals, first confession, first kiss
- `session_16_summary.md` — Sable named, Voss arrested, the speech, the Day 21 incident

### Stored Separately (not in project knowledge)
| Item | Location |
|------|----------|
| Eden's speech at the Voss hearing | Local `.txt` file + Google Doc. Five movements. Key lines in `SESSIONS_5-17_CANONICAL_SUMMARY.md`. |

---

## Session Wrap-Up Procedure

At the end of each session, run the following. It takes two minutes if done immediately; it takes twenty minutes if deferred.

**Step 1 — Update the Current State block above:**
- Increment in-game day
- Update last session title and one-sentence summary
- Update top 3 active threads
- Update next session hook if known

**Step 2 — Add new entities to `ENTITY_INDEX.md`:**
- Any new character who appears more than once gets an entry
- One-line minimum; full entry if they carry plot weight
- Default status: 🔴 Active

**Step 3 — Populate the Review Queue in `ENTITY_INDEX.md`:**
- Flag any entity whose last appearance is now two or more sessions ago for potential demotion
- Flag any Background entity that reappeared for potential promotion
- Flag any Archived entity that resurfaced
- Player confirms all status changes — DM flags, player decides

**Step 4 — Add cross-references if earned:**
- A new cross-reference only if the session revealed a non-obvious connection between two existing entities or threads
- Write the explanation, not just the pointer
- Maximum semantic density — if you can't explain why in one sentence, it's not ready

**Wrap-up prompt** (paste this at session end):
> "Session [N] is complete. In-game day is now [X]. Generate the campaign index update block and entity index additions for this session."

---

## Maintenance Notes

**What stays stable**: The file directory, the wrap-up procedure, the cross-reference rules. Edit these only when the system itself changes.

**What changes every session**: The Current State block. Takes two minutes. Do it before closing the conversation.

**What grows and shrinks**: `ENTITY_INDEX.md`. Grows by addition, shrinks by demotion. Neither the DM nor the player can do the other's half — the DM assesses recency and cross-file presence, the player adjudicates story weight.

**The speech**: Does not need to be in project knowledge. The canonical summary carries what a DM needs. Keep it local.

**Stale file warning**: Quick-start files (`SESSION_6_QUICK_START.md`, `SESSION_7_QUICK_START.md`, etc.) reflect state at the time of writing and are now significantly out of date. Do not load them as current references. They are historical documents.
