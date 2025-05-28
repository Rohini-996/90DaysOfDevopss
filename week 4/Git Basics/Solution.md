#Task 6: Explain Branching Strategies
Document Your Process:
Create (or update) a file named solution.md in your repository.
List all the Git commands you used in Tasks 1–4.
1. Explain: Write a brief explanation on why branching strategies are important in collaborative development. Consider addressing:
. Isolating features and bug fixes
. Facilitating parallel development
. Reducing merge conflicts
. Enabling effective code reviews

Solution: 
The commands i've used in task 1-4 with proper explanation

1. git init
. What it does: Initializes a new Git repository in the current directory.
. Why it's used: Sets up the directory so you can start tracking changes with Git.

2. git add <filename>
. What it does: Adds the specified file to the staging area, preparing it for a commit.
. Why it's used: You stage changes before you commit, allowing precise control over what gets saved in each snapshot.
  Example: git add info.txt

3. git commit -m "message"
. What it does: Saves the staged changes to the repository with a message.
. Why it's used: Creates a checkpoint of your work that you can revisit or roll back to if needed.
  Example: git commit -m "Initial commit: Add info.txt with introductory content"

4. git remote add origin <URL>
. What it does: Connects your local repository to a remote one (usually on GitHub).
. Why it's used: Enables pushing (uploading) and pulling (downloading) code between local and remote.

Example: git remote add origin https://<username>:<PAT>@github.com/<username>/<repo-name>.git

5. git remote set-url origin <URL>
. What it does: Changes the URL of the existing remote named origin.
. Why it's used: To update the remote URL, for instance to include a PAT for authentication.

Example: git remote set-url origin https://Rohini-996:<PAT>@github.com/Rohini-996/90DaysOfDevOps.git
6. git push origin main
. What it does: Uploads local commits to the main branch of the remote repository.
. Why it's used: So your changes are saved on GitHub and accessible to others.

7. git pull origin main
. What it does: Downloads and integrates changes from the remote main branch.
. Why it's used: Keeps your local repository up to date with remote changes.

8. git log
. What it does: Displays the commit history.
. Why it's used: Helps track what changes were made, by whom, and when.

9. git checkout -b <branch-name>
. What it does: Creates a new branch and switches to it immediately.
. Why it's used: To isolate new features or fixes without affecting the main branch.
  Example: git checkout -b feature-update

10. git checkout <branch-name>
. What it does: Switches to an existing branch.
. Why it's used: Allows you to change your working context and view/edit code from another branch.

11. git push origin <branch-name>
. What it does: Uploads the current branch to the remote.
. Why it's used: Shares your new feature or update with others, or prepares it for merging via a Pull Request.


✅ Summary of Git Flow Covered:

1. Initialize repo with git init
2. Track changes using git add and git commit
3. Connect to GitHub with git remote add/set-url
4. Push/Pull code with git push / git pull
5. Branch off using git checkout -b
6. Review history using git log

Git branching startgies i'll explain in my linkdln post of #90DaysOfDevops Challenge
