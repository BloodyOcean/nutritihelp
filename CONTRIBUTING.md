# How to Contribute 🛠️

## Step 1: Find an Issue

Browse the open issues in the main repository and pick one you want to work on.
Or create one if you have found a bug or have a feature request.

## Step 2: Fork the Project 🍴

Click the "Fork" button on the main page of the repository to make a copy in your own account.

## Step 3: Clone the repositry and create a Branch 🌿

Clone repositry:

```bash
git clone <forked_repositry_name>
```

```bash
git switch -c <your_branch_name>
```

## Step 4: Project set-up

### Client side
Open client root directory (nutrihelp_client) and run command in terminal
```bash
npm intall
```
After than you will have successfully established client side of the project.
### Data processing side
For running data processing tasks you will need python 3.10 and jupyterlab
Open data_processing directory and run 
``` bash
pip install -r requirenments.txt
```
Open jupyterlab with all the necessary dependencies and start working.


## Step 5: Work on the Task 👨‍💻👩‍💻

Make the necessary changes in the code or documentation.

## Step 6: Test your code

Make sure that the changes you've made work locally before creating a Pull Request


## Step 9: Commit ✅

Add your changes through Git and create a commit with a descriptive message.

```bash
git add .
```

Create a Commit

```bash
git commit -m 'Your descriptive message'
```

NOTE: Each pull request (PR) should contain only one commit. If you have multiple commits, they need to be squashed.
You can make it using git amend / git push --force

## Commit message stucture
Please, write commit messages in such a format
```
feauture(bug/documentation etc): <short description>
<here you enumerate all the changes were made>
- <Made changes>
- <Made changes>
- <Made changes>
```

**NOTE: Pull request should have the same structure**

## Step 10: Work Remotely 🌍

When your work is ready and complies with project conventions, upload your changes to your fork:

```bash
# Push your work to your remote repository
git push -u origin <your_branch_name>
```

## Step 11: Create a Pull Request ➡️

Go to the page of your fork on GitHub and click "New Pull Request". Verify that the changes are displayed correctly, and then submit your pull request.