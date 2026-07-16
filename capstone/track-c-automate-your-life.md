# 🤖 Capstone Track C — Make the Machine Do a Chore You Hate

> **The mission:** write one small, real Python program that takes over a chore from
> your actual life — planned like Module 04, built like Module 05, versioned like
> Module 08, and tested like Module 09.
>
> **You'll need:** the same free, in-browser Python tool you used in Module 05 (such as
> trinket.io or replit.com — no installation), your GitHub account, and 10–20 hours over
> 2–4 weeks.
>
> **The one rule:** it must be a chore **you actually have**. A program you'll really
> use gets finished; a program for an imaginary person gets abandoned in week two.

---

## 🌶️ Pick your program: the options ladder

Sorted from gentle to spicy. Pick the *lowest* rung that matches a real chore of yours —
remember the capstone rule: slightly too modest is the correct size.

| 🌶️ | Program | What it does | You'll practice |
|---|---|---|---|
| 🌶️ | **Unit converter / recipe scaler** | "This recipe serves 4, I need 7" — enter amounts, get scaled amounts | variables, input, arithmetic |
| 🌶️ | **Random dinner picker (with veto history)** | Suggests dinner from your real list; remembers vetoes so it stops suggesting them | lists, random choice, loops |
| 🌶️🌶️ | **Text cleaner** | Paste messy text (weird spacing, stray line breaks, SHOUTING) — get tidy text back | strings and their methods |
| 🌶️🌶️ | **Habit / study-hours tracker** | Log hours each day; ask for a weekly summary and get totals and a verdict | lists, loops, running totals |
| 🌶️🌶️🌶️ | **Quiz-me flashcards** | Type in question/answer pairs (Spanish words, exam facts); it quizzes you and keeps score | lists of pairs, loops, if/else, score |
| 🌶️🌶️🌶️ | **Expense splitter** | After a group trip: enter who paid what; it says exactly who owes whom | all of the above, plus real logic |

**✅ Checkpoint:** you've picked one and can say the sentence: *"I hate doing ___ by
hand, and this program will do it for me."* If the sentence isn't true, pick again.

## Milestone 1 — Plan first: pseudocode (1–2 hours)

Module 04's discipline. Before touching Python, write your program in **pseudocode** —
numbered plain-English steps precise enough that a patient robot could follow them.
Example for the expense splitter:

```
1. Ask how many people are in the group
2. For each person: ask their name and how much they paid
3. Add up everything paid, divide by number of people
   → that's each person's fair share
4. For each person: what they paid minus fair share
   → positive means they're owed, negative means they owe
5. Print each "X owes Y this much" until everyone is settled
```

Then write **3 user stories** (yes, even for yourself — Module 07): *As the group's
organizer, I want the math done for me, so that nobody argues at the table.* Your
stories decide which features are real and which are decoration.

**✅ Checkpoint:** a friend could read your pseudocode and act it out with paper and a
calculator. That's the test — if they'd get confused at step 3, so will you.

## Milestone 2 — Set up the repo (30 minutes)

1. Create a **public GitHub repository** (e.g. `expense-splitter`), with a README.
2. Put your pseudocode and user stories in the README right now — planning is part of
   the project, and the commit proves you planned *before* building.
3. Open your browser Python tool and start a project there too. You'll build in the
   tool and copy the code into the repo as you go (**one commit per working feature** —
   that's the rhythm).

## Milestone 3 — Build in increments (4–8 hours, in sessions)

The professional rhythm, miniaturized: make the smallest thing that runs, then grow it
one working step at a time. **Never write 50 lines and hope.** For the splitter:

- **Increment 1:** ask for one person's name and amount, print them back. Run it. Works?
  → copy code into the repo, commit: `Read one person's payment`.
- **Increment 2:** a loop for several people, storing amounts in a list. Run. Commit:
  `Collect payments for whole group`.
- **Increment 3:** compute and print the fair share. Run. Commit.
- **Increment 4:** compute who owes whom. Run. Commit.
- **Increment 5:** friendlier wording, a tidy summary at the end. Run. Commit.

Somewhere in there you *will* get stuck — plan on it. That's the
[getting-unstuck protocol](README.md#-the-getting-unstuck-protocol)'s moment: reread,
search the exact error in quotes, rubber duck, then ask your community with a good
question.

**✅ Checkpoint:** your program runs end to end on a real example from your life, and
your repo shows at least 5 feature commits telling the story.

## Milestone 4 — The 5 evil inputs (1–2 hours)

Module 09 time: you are now your own QA engineer. Write a **test plan** — a table of
five deliberately evil inputs, what *should* happen, and what *actually* happens:

| Evil input | Should happen | Actually happened |
|---|---|---|
| Nothing (press Enter on empty) | Polite re-ask, no crash | ? |
| Words where numbers go ("ten") | Polite re-ask, no crash | ? |
| Zero people / empty list | Sensible message, no divide-by-zero crash | ? |
| A negative amount | Rejected or handled — your call, but *decided* | ? |
| Something huge or absurd (a 9-digit expense) | Works, or fails politely | ? |

Your program **will** fail some of these — every program does on the first pass. Fix
what's worth fixing (a crash on empty input: worth it; commit `Handle empty input`).
For the rest, *document* the limitation in the README ("amounts must be plain numbers").
Deciding fix-vs-document is real engineering judgment — Module 09's whole lesson in
one table.

## Milestone 5 — The plain-English README (1 hour)

Rewrite your README so a non-technical human understands it. Include:

1. **What it does**, in two sentences a neighbor would understand.
2. **How to try it** — the link to your trinket/replit project and "press Run".
3. **What I'd add next** — two honest lines (shows judgment, not incompleteness).
4. **Where I got stuck and how I got unstuck** — Module 19 told you this paragraph is
   gold in a portfolio; hiring managers read it as "this person can learn."

## Milestone 6 — Use it for real (ongoing)

Use your program for its actual chore at least twice. Real use will expose one thing you
didn't predict — fix or note it, and commit. Software meeting reality is the last stage
of every lifecycle (Module 07 called it maintenance; now you've *done* it).

---

## ✅ Definition of done

- [ ] Pseudocode + 3 user stories written *before* the code (the commit history proves it)
- [ ] The program runs end to end on a real case from your life
- [ ] Public repo with one commit per feature (≥5 feature commits)
- [ ] Test plan of 5 evil inputs, with crashes fixed or limitations documented
- [ ] README a non-technical person could understand, including the "where I got stuck"
      paragraph
- [ ] You've used it, for real, at least twice 🎉

## ✨ Stretch goal (optional)

**Give it a real user.** Share the trinket/replit link with one human who actually has
the same chore — the spouse who splits the bills, the friend learning Spanish — and ask
them to use it once while you resist the urge to help. Their confusion is free QA; their
"oh, that's handy" is the whole reason software exists. Add what you learned to the
README.

When done: add yourself to the **[Showcase](showcase.md)**. You planned, built, tested,
shipped, and maintained a working program. There's a word for people who do that.
