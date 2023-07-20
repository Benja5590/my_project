# Assignment Task:

- Using Git and GitHub for Version Control

## Objective:

Demonstrate understanding of Git and GitHub by performing various version control tasks using Git commands and GitHub CLI (gh).

## TODO: Steps

1. Initialize a Git repository:

   - Open Visual Studio Code (VSCode).
   - Open the terminal within VSCode.
   - Create a new folder using the following command:
     ```bash
     mkdir my_project
     ```
   - Navigate into the newly created folder:
     ```bash
     cd my_project
     ```
   - Initialize a Git repository in the folder:
     ```bash
     git init
     ```
   - Verify that the repository has been initialized successfully.

2. Create a new file and make initial commit:

   - Create a new file called "index.html" within the project folder using VSCode.
   - Add some basic HTML content to the file.
   - Stage the changes to be committed:
     ```bash
     git add index.html
     ```
   - Commit the changes with a meaningful message:
     ```bash
     git commit -m "Initial commit"
     ```
   - Verify that the commit was successful and the file is now tracked by Git.

3. Connect the local repository to a remote repository on GitHub:

   - Create a remote repo (Note: Replace `name_of_my_project` with your actual repository name.)
     ```bash
     gh repo create name_of_my_project --source=. --public --remote=origin
     ```
   - Verify the remote connection by running:
     ```bash
     git remote -v
     ```
   - Push the local repository to the remote repository:
     ```bash
     git push -u origin master
     ```
   - Provide your GitHub credentials when prompted.

   Reference: [https://cli.github.com/manual/gh_repo_create]

4. Create a new branch and switch to it:

   - Create a new branch called "feature-branch":

   ```bash
   git branch feature-branch
   ```

   - Switch to the newly created branch:

   ```bash
   git checkout feature-branch
   ```

   - Verify that you are now on the "feature-branch" by running:

   ```bash
   git branch
   ```

5. Make changes and commit on the new branch:

   - Open "index.html" in VSCode and make some modifications.
   - Stage the changes:

   ```bash
   git add index.html
   ```

   - Commit the changes with a descriptive message:

   ```bash
   git commit -m "Update index.html on feature-branch"
   ```

6. Push the changes on the feature branch to the remote repository:

   ```bash
   git push -u origin feature-branch
   ```

7. Create additional branches on the command line:

   - Create 4 new branches with the names:
     > - development
     > - team_work
     > - published
     > - collaborators

   Reference: [https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging]

8. Delete the feature branch locally:

   ```bash
   git branch -d feature-branch
   ```

9. Delete the feature branch on the remote repository:
   ```bash
   gh repo branch-delete <repository_name> --branch feature-branch
   ```
   - Note: Replace `<repository_name>` with your actual repository name.
