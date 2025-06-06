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
