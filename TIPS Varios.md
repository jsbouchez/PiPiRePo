TIPS Varios

GITHUB QUICK TIPS

1. Cloning a Repository Locally:

Go to your desired repository on GitHub.
Click the green "Code" button and choose "Clone" or copy the HTTPS URL provided.
Open your terminal or command prompt.
Navigate to your desired local directory using the cd command (e.g., cd Documents/Projects).
Type git clone followed by the URL you copied.
Press Enter. This will create a local copy of the repository on your machine.
2. Updating Your Local Repository:

Make sure you're in the local repository directory (use pwd command to check).
Run git pull in the terminal. This fetches any changes made on the remote repository (GitHub) and merges them into your local copy.
3. Uploading New Files:

Create the new files you want to add in your local repository directory.
In the terminal, run git add <filename> to stage the new file for upload (replace <filename> with the actual filename). You can use git add . to stage all modified files.
Commit the changes by running git commit -m "<message>". Replace <message> with a clear description of your changes.
Push your changes to the remote repository using git push origin main. "main" is the default branch name, you can use the specific branch name if different.
Here are some additional tips:

Use a text editor or IDE familiar with Git for a smoother workflow. Many offer built-in Git functionalities.
Get into the habit of writing clear commit messages. They help track changes and collaboration.
Explore GitHub's visual interface. It allows creating repositories, managing branches, and viewing commit history without needing the command line for everything.

GitBASH QUICK TIPS

1. Getting Started:

Open Git Bash: Search for "Git Bash" in your Windows search bar and launch the application.

2. Navigating Directories:

Use the cd command to change directories. Example: cd Documents/MyProject navigates to the "MyProject" folder within Documents.
Use pwd to check your current working directory.

3. Initializing a Repository:

Navigate to the directory where you want to create your Git repository.
Run git init to initialize a new Git repository in the current directory. This creates a hidden .git folder that tracks changes.

4. Checking Status:

Use git status to see the status of your files. It shows untracked (new) files, modified files, and staged files (ready for commit).

5. Adding and Staging Files:

Use git add <filename> to add a specific file for version control. Example: git add main.py adds the "main.py" file.
Use git add . to add all modified files in the current directory.

6. Committing Changes:

Commit your staged changes with a descriptive message using git commit -m "<message>". Replace <message> with your message (e.g., "Added main script").

7. Cloning a Repository:

Cloning creates a local copy of a remote repository on GitHub.
Find the HTTPS URL of the repository on GitHub.
In Git Bash, navigate to your desired local directory and run git clone <URL>. Replace <URL> with the copied URL.

8. Pushing Changes:

Pushing sends your committed changes to the remote repository on GitHub.
Make sure you've added a remote for the repository using git remote add origin <URL>. Replace <URL> with the remote URL.
Push your changes using git push origin main. "main" is the default branch name. You can use the specific branch name if different.

9. Updating Your Local Repository:

Use git pull to fetch any changes made on the remote repository and merge them into your local copy.
Tips:

Get familiar with basic commands like ls (list files), cp (copy), mv (move), and rm (remove) for managing files within Git Bash.
Use clear and concise commit messages to track changes effectively.
Explore online resources for a more comprehensive understanding of Git commands and workflows.


