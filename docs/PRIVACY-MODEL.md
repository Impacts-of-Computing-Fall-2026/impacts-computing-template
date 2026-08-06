# Repo Access Model (Revised): Private Repos, Real Pseudonymity

This replaces the fork-based workflow. The goal is the same as before —
student autonomy, no corporate LMS dashboard, a real Git workflow — but
without accidentally publishing student work and identities to the internet.

## Why the fork model didn't work

- Forking a public repo on GitHub's free tier always produces a **public**
  fork. There is no private-fork option without paying for GitHub's
  private-forking feature.
- Git commits embed a real name/email by default. A student would have to
  manually reconfigure this correctly, every time, on every machine, or
  their real identity leaks into a public commit log anyway.
- Submitting via PR against the instructor's repo puts every student's
  work, and their (attempted) pseudonym, in one shared public timeline
  visible to the whole class and the world.

## The revised model

**1. One GitHub Organization owns everything.**
Create an org (e.g. `impacts-computing-fa26`). In org Settings →
Member privacy, set membership visibility to **private**. Members of
a private org are not publicly listed as belonging to it.

**2. Repos are created private, per student, from a template.**
Use the `create-student-repos.sh` script from earlier — it already does
this correctly. Each student gets `impacts-computing-<username>`,
private, with only that student (and instructors/TAs) as collaborators.
No forking, no public visibility, nothing crawlable.

**3. Pseudonymity lives in the roster mapping, not in repo visibility.**
Students don't need a separate pseudonymous GitHub account. Since the
repo itself is private, their GitHub username is never exposed to
classmates or the public. What you need instead is a private mapping
you keep **outside** any repo:

```
pseudonym,github_username,real_name,email
convivial_fox,jsmith22,Jamie Smith,jsmith22@school.edu
```

Keep this only in a local spreadsheet or password-protected doc — never
commit it to a repo, even a private one, since repo collaborators can
see it.

**4. Students still scrub their local Git identity, for the *right* reason.**
Not to hide from classmates (the private repo already does that) but to
avoid leaking a personal email into commit metadata that could later be
made public if the repo is ever changed to public, forked forward, or
exported. Each student runs once, in their cloned repo:

```bash
git config user.name "convivial_fox"
git config user.email "jsmith22@users.noreply.github.com"
```

(The `users.noreply.github.com` address is real and provided free by
GitHub to every account — it forwards without exposing the real inbox.)

**5. Submission happens inside the student's own repo, not against yours.**
Students commit directly to their private repo, or open a PR from a
`submission` branch to `main` *within their own repo* if you want a
review step. This avoids ever mixing multiple students' identities into
one shared, browsable list of PRs.

**6. Peer review, if you want it, is handled out-of-band.**
Since repos are now isolated and private, classmates can't naturally see
each other's work (a feature, not a bug, for privacy — but a loss for
peer learning). If peer review matters to your pedagogy, rotate pairs
manually each module and add the paired student as a temporary
collaborator on just that repo for the relevant window, or maintain a
lightweight shared `modules/xx/discussion.md` file per module in a
*separate*, intentionally shared repo used only for discussion threads.

## What changes about the Illich framing

The philosophical point survives, just relocated: convivial tools aren't
defined by *public* visibility, they're defined by the user controlling
their own environment without a corporate intermediary harvesting data.
A private, student-owned Git repo — versus a corporate LMS dashboard —
still delivers that. Public-by-default forking was never required to make
the point, and it was the thing actually undermining student autonomy by
exposing their work without meaningful consent.

## On the Codeberg migration

Consider making the week-8 migration optional or a smaller pilot rather
than a required whole-class event. If you keep it, the private-repo
model transfers directly: Codeberg supports the same private-org,
private-repo pattern, so the mapping and pseudonym setup above doesn't
need to change, just the remote URL.
