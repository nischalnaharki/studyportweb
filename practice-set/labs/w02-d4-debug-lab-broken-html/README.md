# Debugging Lab: Broken HTML
**Phase 1 · Week 2 · Day 4 · 2 hours** · Prereqs: P1.01–P1.03

Momo Express's new page "looks fine" on the owner's laptop. But it has **15 problems**: some break links, some lock out keyboard and screen-reader users, and some are simply invalid HTML. Find as many as you can, fix them, and prove each fix.

## The method (same as Week 1)
**Reproduce → Observe → Form hypotheses → Inspect evidence → Isolate → Fix → Test → Prevent recurrence**

## Your tools
| Tool | How | Finds |
|---|---|---|
| **W3C validator** | validator.w3.org → *Validate by Direct Input* → paste the file | Invalid nesting, missing attributes |
| **Keyboard test** | Mouse away. Tab, Shift+Tab, Enter, Space | Things you can't reach or use |
| **DevTools Network** | Click every link with Network open | 404s and broken paths |
| **Checklist** | `05-accessibility.html` section 3 + `03-forms-and-validation.html` | Labels, alt text, link text |

## Run sheet
| Time | Activity |
|---|---|
| 0:00–0:10 | Open the page with Live Server. Look first: "It looks fine, right?" |
| 0:10–0:30 | Validator pass. Fix what it reports. |
| 0:30–0:55 | Keyboard + Network pass |
| 0:55–1:25 | Checklist pass (headings, labels, semantics, alt, link text) |
| 1:25–1:50 | Pairs swap pages and try to find a bug the other pair missed |
| 1:50–2:00 | Recap: "Which tool found the most? Which bugs did NO tool find?" |

## Scoring (make it a game)
1 point per bug, **found + fixed + proved**. 15 is a perfect score.

## Bug log (one line per bug)
```
# | Line | What was wrong | Who it hurts (everyone / keyboard / screen reader / Google) | Fix | How I proved it
```

## Recap talking points
- The validator found maybe 5–6 bugs. **Most accessibility bugs are valid HTML.** You need the keyboard test and the checklist too.
- "It looks fine" isn't the test. A screen reader, a keyboard, or a Linux server doesn't see what you see.
