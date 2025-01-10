# GitHub Contribution Guide

## Step 1: Clone Your Forked Repository
1. Copy the URL of your forked repository from GitHub (it will be under your account).
2. Clone it to your local machine:

   ```bash
   git clone <your-forked-repo-url>
   ```
   
   **Example:**
   ```bash
   git clone https://github.com/your-username/repository-name.git
   ```

3. Navigate to the repository folder:

   ```bash
   cd repository-name
   ```

---

## Step 2: Add the Original Repository as Upstream
This allows you to keep your fork in sync with the original repository.

1. Add the upstream repository:

   ```bash
   git remote add upstream <original-repo-url>
   ```
   
   **Example:**
   ```bash
   git remote add upstream https://github.com/original-owner/repository-name.git
   ```

2. Verify remotes:

   ```bash
   git remote -v
   ```
   
   **Output should look like this:**
   ```
   origin    https://github.com/your-username/repository-name.git (fetch)
   origin    https://github.com/your-username/repository-name.git (push)
   upstream  https://github.com/original-owner/repository-name.git (fetch)
   upstream  https://github.com/original-owner/repository-name.git (push)
   ```

---

## Step 3: Create a New Branch for Your Task
1. Pull the latest changes from the original repository to keep your fork updated:

   ```bash
   git fetch upstream
   git checkout main
   git merge upstream/main
   ```

2. Create a new branch for your task:

   ```bash
   git checkout -b feature/<task-name>
   ```
   
   **Example:**
   ```bash
   git checkout -b feature/add-user-auth
   ```

---

## Step 4: Work on Your Task
1. Make your code changes in the branch.
2. Test your changes locally.

---

## Step 5: Commit and Push Changes
1. Stage and commit your changes:

   ```bash
   git add .
   git commit -m "Description of the task or fix"
   ```
   
   **Example:**
   ```bash
   git commit -m "Added user authentication feature"
   ```

2. Push the branch to your forked repository:

   ```bash
   git push origin feature/<task-name>
   ```

---

## Step 6: Create a Pull Request (PR)
1. Go to your forked repository on GitHub.
2. You will see a prompt to create a pull request for the branch you just pushed.
3. Click **"Compare & Pull Request"**.
4. Add a title and description of your changes.
5. Submit the pull request to the original repository.

---

## Step 7: Sync Your Fork with the Original Repository (Optional)
If new changes are made to the original repository while you're working, you can sync your fork:

1. Fetch upstream changes:

   ```bash
   git fetch upstream
   ```

2. Merge changes into your branch:

   ```bash
   git merge upstream/main
   ```

3. Resolve any merge conflicts, if necessary, and continue working.

---

## Summary Workflow
1. **Fork** → **Clone** → **Add Upstream** → **Create Branch**.
2. Work on the branch, test, commit, and push.
3. Create a PR from your forked repository to the original repository.

This process ensures your contributions are clean, isolated, and easy to review.

