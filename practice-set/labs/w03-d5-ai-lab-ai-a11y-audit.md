<!-- ============================================================
     AI LAB: AI as an Accessibility Auditor, and Where It Falls Short
     Phase 1 — Week 3, Day 5 (first ~75 min) · Then: w03-d5-weekly-check.md
     By the end, students can:
       - ask AI for a structured accessibility review
       - compare AI findings with Lighthouse and a manual keyboard test
       - identify what each method misses
     Prerequisites: P1.05 Accessibility, Week 2 Debugging Lab (broken HTML)
     Target page: labs/w02-d4-debug-lab-broken-html/index.html (the ORIGINAL broken version)
     ============================================================ -->

# AI Lab: Three Auditors, One Page

## ===== 1. THE SETUP =====

**Notes:** Three ways to audit the same page. Each one catches different things.
| Auditor | Strength | Blind spot |
|---|---|---|
| **AI** (paste the HTML) | Explains _why_, suggests fixes | Can't see the rendered page, can't press Tab, sometimes invents issues |
| **Lighthouse** (DevTools → Lighthouse → Accessibility) | Fast, objective, scores contrast | Catches only rule-checkable issues (~30–40%) |
| **You** (keyboard test + checklist) | Real experience of using it | Slow, and you only catch what you know to look for |

## ===== 2. RUN ALL THREE (pairs, 45 min) =====

**Prompt to use (copy it exactly, then compare results across pairs):**

```
You are an accessibility reviewer. Audit this HTML against WCAG 2.2 level AA.
Return a table: line | problem | who it affects | WCAG criterion | fix.
Only report problems you can see in the code. If unsure, say "unsure".
[paste the broken index.html]
```

Then fill in this table:

| Issue (from the Week 2 answer key, 15 total)  | AI found it? | Lighthouse? | Keyboard/checklist? |
| --------------------------------------------- | ------------ | ----------- | ------------------- |
| 1 … 15                                        |              |             |                     |
| **Extra issues AI reported** (are they real?) |              |             |                     |

✏️ **LIVE CODE:** run Lighthouse . Read the score, then show one bug the score _didn't_ catch.

## ===== 3. VERIFY AI'S EXTRA CLAIMS (15 min) =====

For every issue AI reported that isn't in the answer key:

- Is it **real** (check MDN / the WCAG quick reference), **opinion**, or **invented**?
- Log at least one in your AI log.

⚠️ **Common mistakes**

- "Lighthouse says 100, so it's accessible." Wrong: it can't test keyboard flow, link meaning, or heading logic.
- "AI said it's fine." Wrong: AI never pressed Tab on your page.

## 🧪 TRY IT

1. ★ Total each column. Which auditor found the most? Which found something no one else did?
2. ★★ Ask AI to fix only the 3 most serious issues. Re-run Lighthouse and the keyboard test.
3. ★★★ Write a 5-line "my accessibility review routine" using all three tools in the best order.

## RECAP: ask the class

1. What can AI not do when auditing a page?
2. What % of issues can automated tools catch, roughly?
3. Why ask AI to say "unsure"?
4. Which tool caught the radio-button bug?
5. What's your review routine now?
