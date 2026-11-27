# Debugging Lab: "Why Does It Look Like That?"
**Phase 1 · Week 3 · Day 4 · 2 hours** · Prereqs: P1.07–P1.11

The HTML is fine. **Every bug is in `styles.css`.** The shop owner sent you these complaints:

> 1. "The page title should be our brand red. It's black!"
> 2. "Prices should be **green**. They're red."
> 3. "On my phone I can scroll sideways. Something is too wide."
> 4. "The NEW badge should sit in the corner of the Paneer card. It's floating at the top of the whole page."
> 5. "The tags (Spicy, Veg) should be equal-width pills. They're all different sizes."
> 6. "The dish names are blue like normal links. They should be the same brown as the card text."
> 7. "The footer text is almost invisible, and it's squashed against the edges."

## Rules
- Find the cause in **DevTools first** (Styles, Computed, the box diagram). Write the evidence down **before** you change the file.
- No `!important`. No changing the HTML.

## Run sheet
| Time | Activity |
|---|---|
| 0:00–0:10 | Live Server + open DevTools. Demo: inspect complaint 1 together. |
| 0:10–1:20 | Pairs work through complaints 2–7 |
| 1:20–1:45 | Each pair presents one complaint: evidence → cause → fix |
| 1:45–2:00 | Recap |

## Evidence log
```
Complaint # | DevTools evidence (panel + what you saw) | Root cause | Fix | Lesson file it relates to
```

## Hint ladder (only when stuck 10+ min)
1. Complaint 1: is the property shown with a ⚠️ / crossed out in Styles? Read its name letter by letter.
2. Complaint 2: hover each selector in Styles to see its specificity. Which one wins, and why?
3. Complaint 3: Computed → box diagram of `.card`. Add up width + padding + border.
4. Complaint 4: what is an absolute element positioned relative to?
5. Complaint 5: what `display` is a `span` by default? Does width work on it?
6. Complaint 6: which properties inherit? Does the browser give links their own colour?
7. Complaint 7: Styles shows one strange, crossed-out line in `.footer`. Read it character by character.
