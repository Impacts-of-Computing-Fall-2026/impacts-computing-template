# 🌐 PHL 3100 / MAC 5100: Impacts of Computing
## Asynchronous Course Repository & Sovereign Learning Web

Welcome to the central node for **Impacts of Computing**. This course investigates data enclosure, digital surveillance, platform decay ("enshittification"), and the ethical structures of modern technology.

Rather than using a centralized, commercial corporate dashboard that harvests your student usage data, this course operates as a decentralized workspace running directly on your own hardware.

---

## ⚖️ Theoretical Framework: Convivial vs. Manipulative Computing

This course does not merely study digital ethics from a distance; its physical architecture acts as a living laboratory for the ideas of social philosopher **Ivan Illich**. In his 1973 text [*Tools for Conviviality*](https://archive.org/details/toolsforconvivia0000illi), Illich outlines a critical distinction that governs our infrastructure design:

* **Manipulative (Industrial) Tools:** Technologies designed and enclosed by a corporate elite that strip users of autonomy, enforce conformity, track behaviors, and maximize dependency (e.g., algorithmic timelines, corporate clouds, and centralized, data-harvesting Learning Management Systems).
* **Convivial Tools:** Transparent, accessible infrastructures that give the individuals using them the greatest opportunity to enrich their environment with their own vision. They maximize individual liberty, require no corporate gatekeepers, and encourage localized self-reliance.

Convivial doesn't require *public* — it requires that you, not a corporate dashboard, control your own environment. That's why your workspace in this course is a **private repository you fully own and control**, not a public fork visible to strangers.

---

## 🔒 How Your Repository Works

Each student has their **own private GitHub repository**, created for you before the semester starts. It is not a fork, it is not public, and it will not appear in search engines. Only you and course staff can see it.

### Track A: The Graphical Interface (GitHub Desktop) — recommended for most students

1. **Accept your invitation.** Check your email for a GitHub repository invite and accept it.
2. **Clone Locally:** Open GitHub Desktop, select **File → Clone Repository**, and choose your repository (`impacts-computing-<your-username>`) to download it to your machine.
3. **Commit & Push:** Save your written lab answers into the appropriate weekly directory. Open GitHub Desktop, write a short summary note in the summary box, click **Commit to main**, and click **Push origin** to upload your work. This *is* your submission — there's no separate submit step.

Full walkthrough, including a 5-minute video, is in the Student Guide.

### Track B: The Command-Line Terminal

```bash
# Clone your own private repository
git clone https://github.com/yourorg/impacts-computing-<your-username>.git
cd impacts-computing-<your-username>

# After making changes to a file:
git add .
git commit -m "lab: complete module 01 logs"
git push
```

---

## 🔄 Getting New Modules and Updates

The instructor pushes new modules and lab files directly into your repository as the semester progresses — you don't need to download or place any files yourself. When new material is ready, you'll see an announcement in `class-commons`; after that, just **Fetch origin** then **Pull origin** in GitHub Desktop (or `git pull` on the command line), and the new files appear in your local folder automatically. This only ever adds or updates files the instructor pushes — it never touches your own work.

If you ever have a merge conflict (rare in this setup, since you're the only one editing your own files), **stop and email the instructor** rather than resolving it yourself — a conflict-resolution command applied incorrectly can silently discard your own work.

---

## 💬 Class Discussion

Class discussion happens in **GitHub Discussions**, inside a separate shared repository (`class-commons`) that every student has read-and-comment access to. You're welcome to start your own threads there, not just reply to ones the instructor posts. Note that GitHub Desktop does not surface Discussions notifications — see the Student Guide for how to stay on top of it.

---

## 📝 License

This course curriculum and its interactive laboratories are licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-nc-sa/4.0/). You are free to share, copy, and remix these materials, provided you give appropriate attribution, do not use them for commercial gain, and share any adaptations under these exact same copyleft terms.
