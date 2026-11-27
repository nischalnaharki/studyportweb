<!-- ============================================================
     AI LAB: Reviewing AI-Written CSS
     Phase 1 — Week 4, Day 5 (first ~75 min) · Then: ../w04-d5-weekly-check.md
     By the end, students can:
       - review AI-generated CSS against a checklist
       - turn findings into a precise fix prompt
       - verify the fix at 320px and 1280px instead of trusting it
     Prerequisites: P1.08–P1.16
     ============================================================ -->

# AI Lab: Review AI-Written CSS

`ai-generated.css` is a typical AI answer to *"make a beautiful pricing section for my momo catering"*. On a laptop it looks great. Your job is to **review it like a senior developer.**

## ===== 1. REVIEW CHECKLIST (pairs, 30 min) =====
Open `index.html` at **1280px**, then **375px**. Read every line of the CSS. Mark each item:

| # | Check | Lesson | Pass / Fail + line |
|---|---|---|---|
| 1 | No fixed widths/heights that break on a phone | P1.14 | |
| 2 | Layout uses flow, Flexbox or Grid, not absolute positioning | P1.11–P1.13 | |
| 3 | Keyboard focus is visible | P1.05 | |
| 4 | Text contrast is readable | P1.05 | |
| 5 | No `!important` (except justified accessibility overrides) | P1.08 | |
| 6 | No `transition: all`; motion is purposeful; reduced motion respected | P1.15 | |
| 7 | Fonts it uses are actually loaded | P1.07 | |
| 8 | Units: rem for text, not px everywhere | P1.09 | |
| 9 | Uses tokens (custom properties) and readable class names | P1.16 | |
| 10 | Semantic HTML (bonus: look at `index.html` too) | P1.02 | |

## ===== 2. FIX IT WITH AI, PRECISELY (25 min) =====
❌ "Make it responsive." (too vague: it will invent new problems)
✅ Name each problem, the constraint and the test:
```
Refactor this CSS. Keep the same look on a 1280px screen.
1. Replace absolute positioning + fixed widths with CSS Grid using repeat(auto-fit, minmax(260px, 1fr)).
2. Remove `outline: none`; add a visible :focus-visible style.
3. Body text colour must have at least 4.5:1 contrast on #fafafa.
4. Remove every !important.
5. Replace `transition: all` with specific properties; remove the infinite bounce; add prefers-reduced-motion.
6. Use rem for font sizes and put colours in :root custom properties.
Return only the CSS, then a list of what you changed.
```
Save AI's answer as `ai-fixed.css`, point `index.html` at it, and **re-run the whole checklist**. Did it fix everything? Did it break anything else?

## ===== 3. EXPLAIN IT BACK (15 min) =====
Each pair explains 3 lines of the fixed CSS to another pair, without AI.

## 🧪 TRY IT
1. ★ How many of the 10 checks failed in the original? (The answer key has 10+ findings.)
2. ★★ Find one thing the AI "fix" got wrong or skipped. Add it to your AI log.
3. ★★★ Write the fix yourself without AI, and compare it with AI's version. Which is shorter? Which is clearer?

## RECAP: ask the class
1. Why does "looks great on my laptop" prove almost nothing?
2. Which finding would hurt the most users?
3. What makes a fix prompt "precise"?
4. How did you verify AI's fix?
5. Which of AI's habits will you watch for from now on?
