## A Little History

In 2005, Linus Torvalds — the same guy who created Linux — got fed up with the version control tools available at the time. So he did what any reasonable person would do: he built his own. In about **10 days**.

He called it **Git**. When asked about the name, Linus said:

> "I'm an egotistical bastard, and I name all my projects after myself. First 'Linux', now 'Git'."

("Git" is British slang for an annoying person.)

**Fun facts:**
- Git was built specifically to manage the Linux kernel — one of the largest collaborative software projects in history, with thousands of contributors
- The first version was written in just 10 days, but it was fast enough to handle the entire Linux codebase from day one
- Today, over **100 million developers** use Git worldwide
- Almost every piece of software you use was probably built with Git

## What Is Git?

Git is a **version control system**. Think of it like "Track Changes" in Google Docs, but way more powerful.

It keeps a complete history of every change ever made to a set of files. You can:
- See exactly what changed, when, and who changed it
- Go back to any previous version
- Have multiple people working on the same files without stepping on each other's toes

Without Git, collaborating on a project would look like emailing files back and forth named `website_final_v2_REAL_final_luisedits.zip`. With Git, everyone works from one shared history.

## Git vs. GitHub vs. GitLab

This is where people get confused. They're related but different:

| | What it is |
|---|---|
| **Git** | The tool itself. Free, open source software that runs on your computer. Tracks changes to files. |
| **GitHub** | A website (owned by Microsoft) that hosts Git projects online and adds collaboration features like Pull Requests, Issues, and project boards. |
| **GitLab** | Another website that does the same thing as GitHub, but with a different feature set. Popular with companies that want to self-host. |
| **Bitbucket** | Yet another one, owned by Atlassian (the Jira people). |

**Analogy:** Git is like email (the protocol). GitHub, GitLab, and Bitbucket are like Gmail, Outlook, and Yahoo Mail — different services built on top of the same underlying system.

You can use Git without GitHub, but GitHub without Git doesn't make sense.

The HeatSync Labs website lives on **GitHub**, which is why you'll be using GitHub's web interface to make changes.

## Key Concepts

### Repository (Repo)

A **repository** is a project — a folder of files plus the entire history of changes to those files. The HeatSync Labs website is a repository: [heatsynclabs/new-hsl](https://github.com/heatsynclabs/new-hsl).

### Commits

A **commit** is a saved snapshot of changes. Every time you edit a file and click "Propose changes" on GitHub, you're creating a commit. Each commit has:
- **What changed** (the actual edits)
- **Who made it** (your GitHub account)
- **When** (timestamp)
- **A message** describing the change (e.g., "Fixed typo on about page")

Think of commits like save points in a video game — you can always go back to any of them.

### Branches

This is where it gets interesting.

A **branch** is a separate line of work. Imagine a tree trunk — that's the main version of the website (in our case, the `gh-pages` branch). When you want to make changes, you create a new branch — like a tree branch growing off the trunk.

```
gh-pages (main):     A --- B --- C --- D
                               \
your branch:                    E --- F
```

You make your changes on your branch (`E` and `F`). The main website (`gh-pages`) stays untouched. Other people can also create their own branches at the same time without interfering with each other.

When you edit a file on GitHub, it automatically creates a branch for you (usually named something like `patch-1`). You don't have to think about it — GitHub handles it.

### Forks

A **fork** is your own personal copy of someone else's repository. Since you don't have direct write access to the HeatSync Labs repo, GitHub creates a fork under your account when you edit a file. It's like making a photocopy of a document so you can mark it up without touching the original.

Your fork is connected to the original, so you can easily send your changes back (via a Pull Request).

### Pull Requests (PRs)

A **Pull Request** is how you say "Hey, I made some changes — please review them and add them to the main project."

Here's the flow:
1. You edit files (on your branch, on your fork)
2. You open a **Pull Request** to the original repository
3. A maintainer **reviews** your changes — they can see exactly what you added, removed, or modified
4. If everything looks good, they **merge** it — your changes become part of the live website
5. If something needs fixing, they'll leave a comment and you can update your PR

**Why not just let everyone edit directly?** Because mistakes happen. Pull Requests are a safety net — someone always reviews before changes go live. It's the same reason newspapers have editors.

The name "Pull Request" comes from the idea that you're *requesting* someone to *pull* your changes into their project. (GitLab calls them "Merge Requests" — same thing, arguably a better name.)

## Putting It All Together

Here's what happens when you edit the HeatSync Labs website:

1. You click edit on a file on GitHub
2. GitHub **forks** the repo (makes your personal copy)
3. GitHub creates a **branch** on your fork
4. You make your changes and **commit** them
5. You open a **Pull Request** to send your changes back
6. A maintainer reviews and **merges** your PR
7. The website updates automatically ✨

That's it. That's Git (on GitHub) in 5 minutes.

---

![xkcd: Git](images/xkcd-git.png)

*[xkcd #1597](https://xkcd.com/1597/) — The good news is, using GitHub's web interface means you'll never have to memorize shell commands.*
