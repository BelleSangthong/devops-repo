# Branching strategy

## Chosen strategy

I use short-lived branches for changes that benefit from review, such as documentation and larger changes. These branches are merged into main through pull requests. Since this is currently a solo project, small changes can also be made directly on main when a pull request would add unnecessary overhead. The goal is to keep main stable while keeping the workflow simple.

## Branch protection

In a team, I would protect main by requiring pull requests before merging, blocking force pushes and restricting branch deletion. This reduces the risk of accidentally changing or deleting important history. CODEOWNERS can also be used to identify who should review changes.

## Tagging and versioning

v0.1.0 is the first tagged version. The repository has a branching strategy, a pull request template and a CODEOWNERS file, but no application yet. The 0 in front means everything can still change. The next version number follows from the commit messages: a fix: gives v0.1.1, a feat: gives v0.2.0, and a docs: change does not change the version at all.