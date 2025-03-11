
# SE Assignment 2: Version Control with GitHub

## Project Description
This project is about learning the ins and outs of GitHub. You'll learn how to:
- Create and manage a GitHub repository
- Use branches for different features
- Merge changes and handle conflicts
- Work with pull requests for collaboration
- Keep everything organized and documented with a README and GitHub Issues

## Installation Instructions


1. **Create and Clone the Repository**
   - Go to GitHub.com and create a repository named `SE-assignment2`.
   - Check the option to add a README file.
   - Clone the repository to your computer:

   ```bash
   git clone https://github.com/your-username/SE-assignment2.git
   cd SE-assignment2
   ```

## Usage Examples

### Step 1: First Commit
1. Create a new Python file (`hello.py`) and add this simple program:

   ```python
   print("Hello, World!")
   ```
   We've made a simple file to make it easy to change

2. Save the file, then run these commands to commit and push it to GitHub:

   ```bash
   git add .
   git commit -m "Initial commit with Hello, World!"
   git push origin main
   ```

### Step 2: Working with Branches
1. Create a new branch for a feature:
   ```bash
   git checkout -b feature-1
   ```

2. Edit `hello.py` to ask for user input:
   ```python
   name = input("Enter your name: ")
   print(f"Hello, {name}! Welcome!")
   ```

3. Save and commit the changes:
   ```bash
   git add .
   git commit -m "Added user input feature"
   git push origin feature-1
   ```

### Step 3: Pull Requests and Merging
1. On GitHub, go to the **Pull Requests** tab and click **New pull request**.
2. Choose to merge `feature-1` into `main`.
3. Click **Create pull request**, review the changes, and merge.

### Step 4: Simulating and Resolving Merge Conflicts
1. Switch to the `main` branch and modify `hello.py`:
   ```bash
   git checkout main
   ```

   Edit `hello.py` to say:
   ```python
   print("Hello from MAIN branch!")
   ```

   Then commit and push:
   ```bash
   git add hello.py
   git commit -m "Updated main branch greeting"
   git push origin main
   ```

2. Create a new branch and edit the same file differently:
   ```bash
   git checkout -b feature-2
   ```

   Change `hello.py` to:
   ```python
   print("Hello from FEATURE-2 branch!")
   ```

   Save, commit, and push:
   ```bash
   git add hello.py
   git commit -m "Updated greeting in feature-2 branch"
   git push origin feature-2
   ```

3. On GitHub, open a pull request for `feature-2` into `main`. GitHub will detect a conflict.

### Step 5: Resolving the Conflict
1. Merge `main` into `feature-2` locally:
   ```bash
   git checkout feature-2
   git merge main
   ```

2. Open `hello.py` and resolve the conflict manually:
   ```python
   print("Hello from both MAIN and FEATURE-2 branches!")
   ```

3. Save, commit, and push the resolved file:
   ```bash
   git add hello.py
   git commit -m "Resolved merge conflict"
   git push origin feature-2
   ```

4. Go back to GitHub and finish merging the pull request.

## GitHub Issues
1. On GitHub, go to the **Issues** tab and click **New issue**.
2. Create two issues, like:
   - "Add error checking for user input."
   - "Improve comments in `hello.py`."
3. Assign issues to yourself or a classmate.
4. Close them by referencing them in commit messages:
   ```bash
   git commit -m "Added input validation, closes #1"
   git push origin main
   ```

## Contributors
- [BRegardQ](https://github.com/BRegardQ/SE-assignment2)

