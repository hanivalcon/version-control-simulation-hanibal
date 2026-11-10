# Project Reflection: Version Control Simulation

## Creating and managing branches

I created an empty GitHub repository named `version-control-simulation-hanibal`, without a README, and cloned it. An empty clone has no commits, so `main` did not exist yet and `git checkout main` would have failed. To fix this I made an initial commit on `main` with a README. Then I branched `feature/header` from `main` and built `index.html` with a header and a navigation bar. Next I switched back to `main` and created `feature/footer`, which added a footer. Because both branches started from the same commit, the two features were developed in isolation, as two teammates would work. I used commit messages that say what changed, such as "Added header section to index.html".

## Handling the merge conflict

To set up a conflict, I went back to `feature/header` and changed the footer there: I added "All rights reserved" and a back-to-top link. Merging `feature/footer` into `main` was a fast-forward. Merging `feature/header` then failed with an add/add conflict in `index.html`, since both branches had created the file and both had different footer text. I opened the file and read each block between `<<<<<<<` and `>>>>>>>`. I kept the header, which only existed on one side, and chose the more complete footer. I deleted every conflict marker, ran `git status` to confirm nothing was left unmerged, then staged the file and committed. The merge commit message explains which version I kept and why.

## How pull requests support quality and collaboration

I pushed `main`, then opened a pull request from `main` into `review/main`, a branch that holds the project's starting point. The pull request gathers every change into a single diff with a written description, so a reviewer can see what changed and why before it is accepted. Comments, requested changes and approvals are recorded next to the code, and that history is useful later. Reviewing a classmate's pull request showed me the other side: clear descriptions and small, focused commits make a review faster and more accurate. That is how teams catch mistakes before they reach the main codebase.
