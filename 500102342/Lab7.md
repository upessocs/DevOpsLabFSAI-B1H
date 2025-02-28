Lab 7:

# *GIT Fork and Open-Source*

## Steps:

### 1. Open the desired repository to fork

- Navigate to the repository on GitHub.

### 2. Click on Fork

- Click the *Fork* button in the top-right corner.

### 3. Add a description and create your forked repository

- Provide an optional description.
- Click *Create Fork*.

### 4. Clone the repository locally

```sh
git clone "git@github.com:jahnaviichauhan/DevOpsLabFSAI-B1H.git"
```

### 5. Create a folder with your SAP ID

```sh
mkdir 500102342
cd "./500102342"
```

### 6. Create a README.md file

```sh
touch README.md
```

### 7. Edit the README.md file

```sh
nano README.md
```

### 8. Commit the change

```sh
git add .
git commit -m "Add README.md for Jahnavi Singh Chauhan (500102342)"
git push
```

### 9. Generate a pull request

- Navigate to your forked repository on GitHub.
- Click *Compare & pull request*.
- Provide a meaningful description of your changes.
- Click *Create pull request*.

*Pull request generated, now moderators can review and accept the changes.*



