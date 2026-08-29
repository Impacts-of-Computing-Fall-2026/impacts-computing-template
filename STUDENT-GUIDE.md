# Getting Started: Your Course Repository

Welcome to Impacts of Computing. This course runs on Git and GitHub
instead of a corporate LMS dashboard — you'll be working in your own
private repository for the semester.

You do **not** need prior Git experience. This guide starts with the
fastest possible path to your first successful submission, then covers
the rest once you've seen it work.

---

## Before you start

You should have received an email invitation to a private GitHub
repository named `impacts-computing-<your-username>`. If you haven't
received this, email the instructor with your GitHub username.

If you don't have a GitHub account yet, create one for free at
[github.com/join](https://github.com/join). Use whichever email you'd
like — it does not need to be your school email.

---

## Part 1: Your first five minutes

This section gets you to one real, successful commit as fast as
possible. Everything else in this guide can wait until after you've
seen this work.

1. Download and install [GitHub Desktop](https://desktop.github.com).
2. Sign in with the GitHub account that received the invitation.
3. Click **File → Clone Repository**, select
   `impacts-computing-<your-username>` from the list, and choose a
   location on your computer to save it.
4. Open the folder GitHub Desktop just created. Open `README.md` in any
   text editor and add one line anywhere — even just your name.
5. Save the file, then go back to GitHub Desktop. You'll see the change
   listed. Type a short summary at the bottom left (e.g. "testing my
   setup"), click **Commit to main**, then click **Push origin** at the
   top.
6. Refresh your repository page on github.com. Your change should be
   there.

If you see your change on the website, everything is working. That's
the entire loop you'll repeat all semester: edit a file, commit, push.
There is no separate "submit" button — committing and pushing *is*
submitting.

---

## Part 2: Set your Git identity

Now that you know the loop works, do this one-time setup so your real
personal email address doesn't end up attached to your work.

1. While logged in, go to **github.com/settings/emails**.
2. Find your private "noreply" address — it looks like
   `123456+yourusername@users.noreply.github.com`. Copy it.
3. In GitHub Desktop, go to **File → Options → Git** (or **GitHub
   Desktop → Preferences → Git** on Mac) and set:
   - Name: your real first name, a class nickname, or a pseudonym —
     whatever the instructor's guidance for the semester specifies
   - Email: the noreply address you just copied

This applies to future commits. It won't change the "testing my setup"
commit you already made, and that's fine.

---

## Prefer the command line?

If you're already comfortable with a terminal, you can use Git directly
instead of GitHub Desktop. Everything above still applies conceptually
— clone, edit, commit, push — just via commands:

```bash
git clone https://github.com/yourorg/impacts-computing-<your-username>.git
cd impacts-computing-<your-username>

git config user.name "your-chosen-name"
git config user.email "123456+yourusername@users.noreply.github.com"

# after making changes to a file:
git add .
git commit -m "week 3 discussion response"
git push
```

If this paragraph doesn't already make sense to you, stick with GitHub
Desktop — it does the same thing with no downside.

---

## Getting new modules and updates

The instructor pushes new modules and lab files directly into your
repository as the semester goes on — you don't need to download or
place any files yourself. When new material is ready, you'll see an
announcement in `class-commons`. After that:

**Track A (GitHub Desktop):** click **Fetch origin** at the top of the
window, then **Pull origin** if it appears. The new files show up in
your local folder automatically.

**Track B (command line):** run `git pull` inside your repository
folder.

Either way, this only ever adds or updates the files the instructor
pushes — it never touches or overwrites your own work.

---

## Submitting Analyst Format labs

If you choose the Analyst Format for a given week's lab (see
SYLLABUS.md §4), your deliverable is a `LAB-SUBMISSION.md` file. Start
from `LAB-SUBMISSION-TEMPLATE.md` at the root of your repository — it
has instructions at the very top (as an HTML comment, visible when you
open the raw file) covering exactly how to copy, rename, and save it
inside that week's module folder so nothing gets overwritten as the
semester goes on.

---

## Class discussions

All class discussion happens in a separate shared repository called
`class-commons`, using GitHub's **Discussions** feature — not in your
own private repo. You were added to it with read and comment access
when your repos were set up; find it at
`https://github.com/yourorg/class-commons`, under the **Discussions**
tab.

You can start new threads there yourself, not just reply to ones the
instructor posts — this space is for you to raise questions, share
resources, or respond to classmates as you see fit.

**Important: GitHub Desktop will not notify you about Discussions
activity.** Its notifications only cover pull requests in your own
repo, so a reply to your thread won't show up there the way a push
does. To stay on top of it:

1. Go to `https://github.com/yourorg/class-commons`, click **Watch**
   near the top of the page, and make sure notifications are turned on
   for that repo. This routes updates to your email.
2. Since email notifications aren't always reliable or immediate, get
   in the habit of checking the Discussions tab directly every few days
   rather than waiting to be pinged — especially in weeks when a
   discussion is part of your assignment.

---

Your repository is **private** — it is not a fork, it is not public, and
it will not show up in search engines or be visible to classmates. This
is intentional: what you write here is coursework, not a public
portfolio, unless a specific assignment tells you otherwise.

To be specific about who can see it: the instructor (and any co-instructors
listed as course staff) has standing access to every student's repository
by default, as a consequence of how the course organization is set up —
not because it's individually granted per assignment. This is the same
kind of access an instructor already has to your work in a gradebook or
LMS. Any teaching assistants only have access if they're explicitly added,
and that will be disclosed to you if it applies this semester.

One exception: the **Exposure Lab** (Module 0x) is a separate, opt-in
exercise that deliberately uses a throwaway account to explore what
*does* happen when something is public. Instructions for that are
separate from this guide, and nothing from your real course repo is
ever involved in it.

---

## If something goes wrong

- **"I get a permission denied error when I push."** Make sure you
  accepted the repository invitation via the email GitHub sent you, and
  that you're logged into the GitHub account the invitation was sent to.
- **"I have a merge conflict."** This is rare in this workflow since
  you're the only one editing your repo, but if it happens, stop and
  email the instructor rather than force-pushing or deleting files —
  it's usually a two-minute fix on our end.
- **General Git confusion:** email the instructor or bring your laptop
  to office hours. There's no such thing as a bad question here — this
  is likely new for most of the class.
