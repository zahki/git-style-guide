# Git Style Guide
Git styleguide followed here at Zahki.

## Commits

- Each commit should be a single logical change. Don't make several logical changes in one commit. 

    > For example, if a `patch` fixes a bug and optimizes the performance of a feature, split it into TWO SEPARATE COMMITS.
    > Tip: Use `git add -p` to interactively stage specific portions of the modified files.

- Don't split a single logical change into several commits. 

    > For example, the implementation of a feature and the corresponding tests should be in the same commit.

- Commit early and often. Small, self-contained commits are easier to understand and revert when something goes wrong.

- Commits should be ordered logically. 

    > For example, if commit X depends on changes done in commit Y, then commit Y should come before commit X.
    
- ALWAYS guarantee that the master branch only contains commits that are fully functional, have their own tests and fixes.

    > **Note:** While working alone on a local branch that has not yet been pushed, it's fine to use commits as temporary snapshots of your work. However, it still holds true that you should apply all of the above before pushing it to remote. To do that it's really important to understand `git rebase -i`.

```sh
    # good
    $ git commit

    # bad: no commit message
    $ git commit -m "Just a quick fix"
```
