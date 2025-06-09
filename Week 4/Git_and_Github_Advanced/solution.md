#Task 1
Document in solution.md
<br>
. Steps to create a PR.
<br>
. Best practices for writing PR descriptions.
<br>
. Handling review comments.

Solution: 

✅ Steps to Create a Pull Request
. Create a new branch
. git checkout -b feature-branch
. Make your changes

Keep commits focused and meaningful.

Test your changes locally.

Add and commit your work

. git add .
. git commit -m "Added a new feature"
. Push to the remote branch
. git push origin feature-branch

Open a Pull Request (PR)
Go to GitHub.
Click "Compare & pull request".
Choose the correct base branch (usually main).

Fill in the PR title and description.

✅ Best Practices for Writing PR Descriptions
Your PR description is the why behind the what. A good one helps reviewers understand your intent quickly.

A good format:
## What
Briefly explain what the PR does.

## Why
Explain the reasoning or the problem this PR solves.

## How
Optional: Outline how the problem is solved, especially if the approach is non-trivial.

## Screenshots / Demo
Optional: Add UI screenshots, links to live previews, or code snippets.

## Checklist
- [ ] Tests added or updated
- [ ] Docs updated (if needed)
- [ ] Ready for review
 
✨ Tips:
. Keep it clear and concise.
. Use bullet points for readability.
. Reference issues or tickets: Fixes #123, Closes [JIRA-456].

✅ Handling Review Comments

Code reviews are a conversation. Here’s how to keep it constructive and collaborative.

If you agree with the feedback:

Thank the reviewer.
Make the changes.
Push updates.

git add .
git commit -m "fix: updated logic based on review"
git push

If you disagree:
Be respectful and explain your reasoning.
Offer alternatives if possible.
Remember: it’s not personal — it’s about the code.

For reviewers:
Be specific in your comments.
Suggest, don’t command.
Encourage when things are done well.

🔄 After Changes

Once you’ve addressed feedback:
Leave a comment like:
“Thanks! Changes pushed, please take another look. 🙌”
Wait for approval ✅
Merge using the team's preferred method


#Task 2 
Document in solution.md
<br>
Differences between reset and revert.
<br>
When to use each method.
<br>

Solution:
📄 Differences Between git reset and git revert

🔁 git reset – Rewriting History
What it does:

1. Moves the HEAD pointer and removes commits from the history.

2. Can also modify the staging area and working directory depending on the mode:

3. --soft: Keeps changes staged.

4. --mixed: Keeps changes in the working directory, unstaged.

5. --hard: Deletes changes from both the working directory and staging area.

When to use it:

. You made a mistake in your local repo and haven't pushed the commit yet.

. You want to modify the commit (e.g., change the message or files).

. You’re okay with rewriting history.

⚠️ Warning:
Never use reset on commits that have already been pushed/shared with others — it rewrites history and can cause conflicts.

🔄 git revert – Undo with a New Commit
What it does:

1. Creates a new commit that reverses the changes introduced by a previous commit.

2. Does not remove the original commit from history.

3. Safe to use on shared/public branches.

When to use it:

. You need to undo a commit that has already been pushed.

. You want to preserve a clean and traceable history.

. You're collaborating with others and need to avoid rewriting history.

✅ Safe and clean:
This is the recommended method when working on shared repositories or teams.

#Task 3
<br>
Document in solution.md
<br>
1 When to use git stash.
<br>
2 Difference between git stash pop and git stash apply.
<br>

Solution:

1. When to Use git stash

. Use git stash when you have uncommitted changes (staged or unstaged) but need to:
<br>
. Switch branches temporarily
<br>
. Pull updates from a remote branch without merge conflicts
<br>
. Test something else without losing your current work
<br>
. Keep your working directory clean while debugging or exploring
<br>
. It allows you to save your current progress without committing, so you can safely return to it later.
<br>

2. Difference between git stash pop and git stash apply.

1 git stash pop
<br>
. git stash pop also puts your saved changes back, but it removes those changes from the stash list after applying them.
<br>
. Use git stash pop if you want to restore and delete the stash in one step.
<br>
. Use git stash pop to restore changes and delete stash
<br>

2 git stash apply
<br>
. git stash apply puts your saved changes back into your working files, but it keeps a copy of those 
  changes saved in the stash list.
  <br>
. Use git stash apply if you want to reuse the stash later.
 <br>
. Use git stash apply to restore changes but keep stash.
 <br>
. git stash apply can apply the same stash multiple times if needed.

#Task 4
<br>
Document in solution.md
<br>
How cherry-picking is used in bug fixes.
<br>
Risks of cherry-picking.
<br>

1 What Is Cherry-Picking in Git?
<br>
<br>
. Cherry-picking means taking one specific commit from one branch and applying it to another. You use this when you only want a particular       change, not everything from a branch.

. This is especially useful when fixing bugs.

. How It Helps with Bug Fixes
  <br>
  Let’s say a developer fixed a bug in a branch called bugfix-branch, but that branch isn’t ready to be merged into main yet.

Instead of waiting, you can cherry-pick just the bug fix commit into main so it can be released right away.

✅ Example
<br>
git checkout main
<br>
git cherry-pick abc1234
<br>
Here, abc1234 is the commit hash of the bug fix you want to apply.

2 ⚠️ Risks of Cherry-Picking
<br>
Cherry-picking is powerful but should be used with care. Here are the main things to watch out for:

1. Merge Conflicts

If the code in the two branches is very different, Git might not know how to apply the changes. You’ll get a conflict and will need to fix it manually.

3. Missing Context
   
. Sometimes, a bug fix depends on other code changes that weren’t cherry-picked. Without them, the fix might break or not work at all.

. Example: The fix uses a helper function that doesn’t exist in the target branch. That will cause an error.

3. Confusing Git History
   
. A cherry-picked commit is treated as a new commit with a different ID. This can make the history look messy and confusing, especially if the   original branch is merged later.

5. Harder Future Merges
   
. If you later merge the original branch into your current one, Git might not realize the fix was already applied. You could get conflicts or    duplicate code.

7. More Maintenance
   
. When you cherry-pick often, it becomes harder to keep track of which fixes went where. Teams may forget or duplicate work without
  realizing it.




