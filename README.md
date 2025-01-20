# Tracking changes with git

In this activity we will track and manage changes to a repository using git. We will do this using the command line interface (CLI). Follow the steps below to complete the activity and complete the extension if you have time.

## 👣 Steps

1. First, open **Git Bash**. Then navigate to your workspace and make a new folder (let's call it tracking-changes-git).

    `mkdir tracking-changes-git`

    `cd tracking-changes-git`

   <br/>

3. Second, let's configure git and tell it who we are:

   `git config --global user.name "Your GitHub username"`

   `git config --global user.email "Your email address"`

   <br/>

5. Now, before we begin, let's check the status of our repository using the status command:

    `git status`

    Can you explain the message that is returned after running the command?

    <br/>

6. Make a repository using the init command:

    `git init`

    After running the command you should see a message beginning:

    `Initialized empty Git repository in`

    This message means we have successfully created a repository!

    Can you confirm the repository has been created using the status command?

    <br/>

7. Lets check the history (versions) of our repository using another command:

    `git log`

    <br/>

8. Before we make our first commit. We first need to make a change to the repository. So let's make a new file:

    `touch an-empty-file.txt`

    Optionally, confirm that the file has been created and check the contents of your folder with:

    `dir`

9. Now that we have made a change, let's make a commit to record it in the history of the repository:

    `git commit`


    After running the command, you will have seen a message like this:

    ```
    On branch main

    Initial commit

    Untracked files:
    (use "git add <file>..." to include in what will be committed)
            an-empty-file.txt

    nothing added to commit but untracked files present (use "git add" to track)
    ```
    
    The message is telling us that there is nothing to commit and that we need to use `git add` instead. This is because our file is not in our index (staging area). Files are not added to this area automatically upon their creation.

    Why?

    Well, although it might seem needless at first. Having a staging area can be useful in practice; if we had made changes to multiple files, we might not want to record all of them in a single commit, and in this case we could use the staging area to arrange a series of logical commits.

    <br/>

9. This time, let's add the file to our staging area first, and then make a commit:

    `git add an-empty-file.txt`

    `git commit -m "Add an-empty-file.txt"`

    The first command adds our file to the staging area and the second records a change/commit on our local branch. With the `-m "Add an-empty-file.txt"` part of the second command, we are specifying the commit message. Git expects a message to be included with a commit and would prompt us for one if we did not specify.

   <br/>

10. To conclude, let's view the history of this repository and confirm that the change was recorded:

    `git log`

    The message returned should look like:

    ```
    Author: Your credentials
    Date:   Day Month d HH:MM:SS yyyy

        Add an-empty-file.txt

    ```

🎉 Well done! You have now tracked and managed changes to a repository using git. We have focused on our local repository so far and will explore pushing to and pulling from a remote repository in the next activity.

## 🔌 Extension

Experiment with the different git commands and build your understanding of them. Add additional files and make changes to existing files. Record the changes using `git add` and `git commit`. At various points, use `git status` and `git log` to observe the impact the other commands have on the repository.
