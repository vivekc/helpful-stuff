- Issue titles should describe the desired state of the system, e.g. "As an administrator I want to remove users without receiving an error" instead of "Admin can't remove users.".
- When you are ready to code you start a branch for the issue from the master branch. The name of this branch should start with the issue number, for example ```'15-require-a-password-to-change-it'```
- When you are done or want to discuss the code you open a merge request. This is an online place to discuss the change and review the code. Opening a merge request is a manual action since you do not always want to merge a new branch you push, it could be a long-running environment or release branch. If you open the merge request but do not assign it to anyone it is a 'Work In Progress' merge request. These are used to discuss the proposed implementation but are not ready for inclusion in the master branch yet. Pro tip: Start the title of the merge request with ``[WIP]`` or ``WIP:`` to prevent it from being merged before it's ready.

- When the author thinks the code is ready the merge request is assigned to reviewer. The reviewer presses the merge button when they think the code is ready for inclusion in the dev branch. In this case the code is merged and a merge commit is generated that makes this event easily visible later on. Merge requests always create a merge commit even when the commit could be added without one. This merge strategy is called 'no fast-forward' in git. 
- After the merge the feature branch is deleted since it is no longer needed, in GitLab this deletion is an option when merging.

- Suppose that a branch is merged but a problem occurs and the issue is reopened. In this case it is no problem to reuse the same branch name since it was deleted when the branch was merged. At any time there is at most one branch for every issue. 
It is possible that one feature branch solves more than one issue.

- Linking to issues can happen by mentioning them in commit messages (fixes #14, closes #67, etc.) or in the merge request description. GitLab then creates links to the mentioned issues and creates comments in the corresponding issues linking back to the merge request. These issues are closed once code is merged into the default branch.

