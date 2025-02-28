Git Submodules: Managing Multiple Repositories
Overview
This guide covers how to:

Clone multiple repositories
Create and manage files
Add and commit changes
Set up Git submodules
Push updates to remote repositories
Step 1: Cloning Repositories
You cloned three repositories from GitHub:

sh
Copy
Edit
git clone https://github.com/piyush95881/Demo-main.git
git clone https://github.com/piyush95881/Demo-css.git
git clone https://github.com/piyush95881/Demo-js.git
💡 Note: A typo (gir clone instead of git clone) was encountered earlier. Ensure the correct command is used.

Step 2: Creating Files in Each Repository
Navigate to each repository and create the necessary files.

In Demo-js repository
sh
Copy
Edit
cd Demo-js
touch script.js
In Demo-css repository
sh
Copy
Edit
cd ../Demo-css
touch style.css
In Demo-main repository
sh
Copy
Edit
cd ../Demo-main
touch index.html
Step 3: Committing and Pushing Changes
For each repository, the changes were staged, committed, and pushed.

For Demo-main
sh
Copy
Edit
git add .
git commit -m "added main"
git push
For Demo-js
sh
Copy
Edit
git add .
git commit -m "added js"
git push
For Demo-css
sh
Copy
Edit
git add .
git commit -m "added css"
git push
Step 4: Setting Up Git Submodules
You added Demo-css and Demo-js as submodules inside Demo-main:

sh
Copy
Edit
git submodule add git@github.com:piyush95881/Demo-css.git css
git submodule add git@github.com:piyush95881/Demo-js.git js
Then, commit and push the changes:

sh
Copy
Edit
git commit -m "added css to main"
git push

git commit -m "added js to main"
git push
Step 5: Updating index.html
After modifying index.html to correct file paths, you committed and pushed the changes:

sh
Copy
Edit
git add .
git commit -m "updated html with correct paths"
git push
Step 6: Verifying Repository Status
Check the repository status to ensure everything is up to date:

sh
Copy
Edit
git status