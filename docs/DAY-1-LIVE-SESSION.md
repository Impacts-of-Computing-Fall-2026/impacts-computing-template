# Day 1: Live Kickoff Session

## PHL 3100 / MAC 5100 – Impacts of Computing

**Format:** Synchronous, ~75–90 minutes. This is the one live session in an otherwise asynchronous course — its job is to get everyone unstuck on setup together, not to re-teach material that's already written down. Favor doing things live over explaining them.

**Before this session:** every student should have completed `PREREQUISITES.md` — GitHub account created, username submitted via the pre-semester form, Git installed. If someone hasn't, they can still follow along and catch up live; don't block the session on stragglers.

**Instructor prep — important:** do **not** run `create-student-repos.sh` before this session. Running it live is now part of the demonstration (see Section 2) — if it's already been run, students' repos will already exist and the live run will just print "already exists, skipping" for everyone, which defeats the point. Have your `students.csv` finalized and ready to go, but hold off executing the script until you're live with the class.

---

## 1. Framing (5–10 min)

Keep this short — the full philosophical grounding is in `SYLLABUS.md` §1 and `README.md`, and students can (and should) read it on their own.

Say enough to set tone:
- This course studies data enclosure, surveillance, and platform decay — and its own infrastructure is a small working example of the alternative (Illich's "convivial tools").
- That's why we're not using Brightspace for weekly work: a private Git repository you control, instead of a corporate dashboard tracking you.
- Everything from here forward is spent *doing*, not listening.

---

## 2. Watching the Automation Run (10–15 min)

This is the new segment — showing students the actual infrastructure
getting built, live, rather than arriving with it already done for
them.

1. Share your screen and open a terminal in the folder with
   `create-student-repos.sh` and your finalized `students.csv`.
2. Briefly explain what's about to happen: one private repository per
   student, created from the course template, plus a shared
   `class-commons` repo for discussion — all in one script run.
3. Run it:
   ```bash
   ./create-student-repos.sh students.csv YOUR-ORG/impacts-computing-template YOUR-ORG
   ```
4. Narrate the output as it prints — "Created ✓" for each student,
   `class-commons` creation, Discussions being enabled. This is the
   actual moment of "magic" — let it breathe rather than talking over
   every line.
5. **Budget a few minutes of buffer after it finishes.** GitHub's
   invitation emails aren't always instant — while everyone waits for
   theirs to land, this is a good moment to explain in plain language
   what a commit and a push actually are, since you're about to do
   both live in the next section.

**Facilitator note:** if the script errors on any individual row
(typo'd username, someone who registered late), don't let it derail
the room — the script continues past failed rows automatically. Note
who failed, keep going, and follow up with that student 1:1
afterward — see the facilitator note in the next section for the
same underlying issue.

---

## 3. Live First Commit (15–20 min)

Do this together, step by step, live — this mirrors Student Guide Part 1 exactly, and is the highest-value block of the session. Screen-share your own screen doing it once, then have everyone do it themselves in real time while you circulate (verbally, in chat, or breakout rooms) to catch anyone stuck.

1. Confirm everyone has accepted the repository invitation email that just arrived from Section 2.
2. Everyone opens GitHub Desktop, signs in, and clones their own `impacts-computing-<username>` repo.
3. Everyone opens `README.md` locally, adds one throwaway line (their name is fine), and saves it.
4. Everyone commits ("testing my setup") and pushes.
5. Everyone refreshes their repo page on github.com and confirms the change is live.

**Facilitator note:** the most common failure point is step 1 — someone whose row failed in Section 2 (typo'd username, didn't submit in time). Fix these individually after the session using `create-student-repos.sh` with just their corrected row — don't hold up the room for it.

---

## 4. Identity Setup (5 min)

Quick and mechanical — Student Guide Part 2. Walk through it live since it's easy to fumble alone:

1. Everyone finds their GitHub noreply email at `github.com/settings/emails`.
2. Everyone sets it, plus their chosen class handle, in GitHub Desktop's Git preferences.

No need to linger here — confirm everyone's done it, then move on.

---

## 5. Tour of `class-commons` (5–10 min)

1. Share your screen and navigate to the `class-commons` repo's Discussions tab.
2. Explain in one sentence: this is where all class discussion happens, separate from your private repo.
3. Have everyone post one throwaway message right now — literally "hello, this is [handle]" is fine. The goal is that everyone has posted *something* before the session ends, so the first post ever doesn't happen alone, days later, with no context.
4. Mention the GitHub Desktop notification gap from the Student Guide: Discussions replies won't show up there, so they'll want to turn on email notifications for this repo specifically.

---

## 6. This Week's Task, and a Preview of What's Next (5–10 min)

**This week is Module 0** (`modules/00-exploring-the-repository.md`) —
ungraded, pass/fail. Students spend the week exploring their own repo
and posting a genuine first reaction to the "convivial tool" claim in
`class-commons`, before any of the theory arrives. Walk through what
that actually involves:

- Browse `docs/`, `labs/`, `modules/` — just look, nothing to run yet
- Write a short, honest first reaction: does this feel like a
  convivial tool, or not, and why?
- Post it as a real thread in `class-commons` (not the throwaway
  "hello" from step 3) and reply to at least one classmate

Then, open `modules/01-foundations-decentralization-minimal-computing.md`
together as a preview of what a normal content week looks like starting
next week — without going deep on its actual content, that's their
reading for Week 2:

- Readings at the top
- Theoretical context in the middle
- A choice at the bottom: **the Developer Format** or **the Analyst
  Format** — remind them this is a different choice from GitHub
  Desktop vs. command line (that's Track A/B), and they can pick a
  different format each week
- Where labs live (`labs/`) and what a submission file
  (`LAB-SUBMISSION.md`, copied from the template) looks like

---

## 7. Privacy Model, Stated Plainly (5 min)

Say this out loud, don't just point to the doc:

- Your repository is private. It is not a fork, not public, not indexed by search engines.
- The instructor (and any listed course staff) has standing access to every repo, as a structural consequence of how the course organization works — the same kind of access an instructor has to a gradebook.
- Later in the semester, there's an **optional** Exposure Lab where you can choose to experience what public *does* mean, using a throwaway account — nothing from your real coursework is ever involved in that.

---

## 8. Open Floor (remaining time)

Individual troubleshooting — this is the actual point of having a live session at all. Let people ask anything, including things that feel too basic to email about.

---

## What's intentionally NOT in this session

- **No GPG key generation.** Not part of this course's infrastructure.
- **No forking instructions.** Repos are created for students directly; there's nothing to fork.
- **No Codeberg / migration talk.** That's an optional week-8 aside covered in `docs/MAINTENANCE-NOTICE.md` — raising it here just adds anxiety about something eleven weeks away, for an exercise most students won't opt into.
