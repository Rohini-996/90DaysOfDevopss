Task 1
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


Task 2 
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
