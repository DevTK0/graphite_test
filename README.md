# Intro
This repository is for experimenting with git flows.

# Experiments
## Rebase
What happens when you do a rebase merge in the github editor?

- It merges all the commits onto the head of the main branch.
- Anyone else that pulls from remote will need to handle merges.

How do you handle merges without having merge commits?
- Don't share branches.
- Changes should all be in their own respective feature branches.
- Only merge through PRs.

## Graphite

### Split
Can you select only specific commits to split into a new PR and leave the rest in the original once?
- Yes. You can select the destination branch of the commits. Just use the original branch for the commits you want to keep.

What happens if you split out all of the commits?
- The original PR will still retain all of the original commits and new branches will be created pointing to the same original commits. (i.e. it's duplicated)

### Stacked Diffs
What happens when I add a commit to a mid stack?
- Graphite will automatically restack after modifying the stack and prompt you to resolve the merge conflicts. Alternatively, you can run absorb to automatically accept the latest commits.