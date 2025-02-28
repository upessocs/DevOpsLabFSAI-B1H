GIT Fork and Open-Source Contribution Guide
Follow these steps to fork a repository, make changes, and submit a pull request on GitHub.

Step 1: Fork the Repository
Navigate to the desired repository on GitHub.
Click the Fork button in the top-right corner.
Provide an optional description.
Click Create Fork to create a personal copy of the repository.
Step 2: Clone the Forked Repository Locally
Run the following command to clone your forked repository:

sh
Copy
Edit
git clone "git@github.com:your-username/DevOpsLabFSAI-B1H.git"
Replace your-username with your actual GitHub username.

Step 3: Create a Folder with Your SAP ID
Navigate into the cloned repository and create a folder using your SAP ID:

sh
Copy
Edit
mkdir 500107002
cd 500107002
Step 4: Create and Edit the README.md File
Create a README.md file:

sh
Copy
Edit
touch README.md
Open and edit the file using nano:

sh
Copy
Edit
nano README.md
Add your content, then save and exit (CTRL + X, then Y, then Enter).

Step 5: Commit and Push the Changes
Stage the changes:

sh
Copy
Edit
git add .
Commit with a meaningful message:

sh
Copy
Edit
git commit -m "Added my folder and README.md"
Push the changes to your forked repository:

sh
Copy
Edit
git push
Step 6: Generate a Pull Request (PR)
Navigate to your forked repository on GitHub.
Click on Compare & pull request.
Provide a meaningful title and description of your changes.
Click Create pull request