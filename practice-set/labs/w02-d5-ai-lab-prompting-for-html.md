<!-- ============================================================
     AI LAB: Prompting for HTML, then Auditing What You Get
     Phase 1 — Week 2, Day 5 (first ~75 min) · Then: w02-d5-weekly-check.md
     By the end, students can:
       - write a context-rich prompt (role, level, constraints, format)
       - audit AI-written HTML with the validator, keyboard test and checklist
       - log what AI got wrong
     Prerequisites: P1.01–P1.03, Week 1 AI lab (AI as a tutor)
     ============================================================ -->

# AI Lab: Prompting for HTML

## ===== 1. CONTEXT MAKES THE ANSWER =====

**Notes:** AI fills every gap with guesses. Give it the gaps.

| Part             | Example                                                                                      |
| ---------------- | -------------------------------------------------------------------------------------------- |
| **Role / level** | "I'm a beginner in week 2 of a web course."                                                  |
| **Goal**         | "I need a contact page for a momo shop in Thamel."                                           |
| **Constraints**  | "HTML only, no CSS or JS. Semantic elements. Every input has a label. No div unless needed." |
| **Format**       | "Give me the full file, then a bullet list explaining each element you chose."               |

⚠️ **Common mistake**

- ❌ `make a contact page` → divs, Lorem ipsum, invented frameworks, CSS you didn't ask for
- ✅ The 4-part prompt above

## ===== 2. GENERATE, THEN AUDIT (pairs, 40 min) =====

1. Pair A uses a **one-line** prompt. Pair B uses the **4-part** prompt. Same goal: _"StudyPort course enquiry page with a form."_
2. Save each result as `ai-v1.html` (one-liner) and `ai-v2.html` (4-part).
3. Audit **both** with this checklist:

| Check                                                      | Tool            | ai-v1 | ai-v2 |
| ---------------------------------------------------------- | --------------- | ----- | ----- |
| Valid HTML (0 errors)                                      | W3C validator   |       |       |
| `lang`, viewport, real title                               | Read the head   |       |       |
| Landmarks (`header`/`main`/`footer`)                       | Read / Elements |       |       |
| One h1, no skipped levels                                  | Read            |       |       |
| Every input has a `label`                                  | Keyboard + read |       |       |
| Phone is `type="tel"`                                      | Read            |       |       |
| Radios share a name, inside a `fieldset`                   | Keyboard        |       |       |
| Real `<button type="submit">`                              | Keyboard        |       |       |
| Did it add things you didn't ask for? (CSS, JS, CDN links) | Read            |       |       |

4. Ask AI to fix **one** problem by naming it exactly: _"Input #phone has no label. Add a visible label linked with for/id. Change nothing else."_ Then re-check that it really changed nothing else.

✏️ **LIVE CODE:** run both prompts . Validate both results live.

## ===== 3. EXPLAIN IT BACK (15 min) =====

Pick 5 elements from the AI page. Without AI, explain to your partner **why** each one is there. If you can't explain it, you can't submit it (AI Independence Rule 1).

## 🧪 TRY IT

1. ★ Add 2 entries to your AI log: something AI did well, and something it got wrong.
2. ★★ Write your own reusable "HTML page prompt template" with the 4 parts.
3. ★★★ Ask AI to "make this page accessible", then find one thing it claimed to fix but didn't.

## RECAP: ask the class

1. What are the 4 parts of a good prompt?
2. Which version (one-liner or 4-part) had fewer problems? By how many?
3. Why name the exact problem when asking for a fix?
4. What did AI add that nobody asked for?
5. What's AI Independence Rule 1?
