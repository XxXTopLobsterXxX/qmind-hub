# Git/Github Workflow Assignment

The purpose of this assignment is to familiarize team members with the Git/Github workflow, which we will be using throughout the year for version control and collaboration.

# Part A: Creating a local repository

1. If you have not already installed Git on your computer, follow this [guide](https://www.linode.com/docs/development/version-control/how-to-install-git-on-linux-mac-and-windows/).

2. Once you have Git installed, open a Terminal window. You can do this by opening [Terminal](http://blog.teamtreehouse.com/introduction-to-the-mac-os-x-command-line) on Mac, or [Command Prompt](https://www.digitalcitizen.life/7-ways-launch-command-prompt-windows-7-windows-8) on PC

3. Verify that your Git is correctly installed by typing "git" and pressing Enter

4. Create a new folder using the following command

```bash
    mkdir my-example-repo
```

5. Change into the new folder using:

```bash
    cd my-example-repo
```

6. Turn the new folder into a git repository using:

```bash
    git init
```

7. Make a text file called `example.txt` in the project folder. You can open up a file explorer in the project using

```bash
    open .
```

8. Write some text in this file using a text editor of your choice and save the file

9. Now go back to your terminal window and execute the following commands:

```bash
    git add .
    git commit -m "First commit"
```

10. You have now created your first commit! You can see this by executing

```bash
    git log
```

> NOTE: To exit the text window you will need to enter `:q`

# Part B: Connecting to Github

1. If you do not already have an account, create a Github account

2. Once you have an account, go to your profile and click on the `repositories` tab, and click the `new` button.

3. Enter a name and a description for your remote repository, the name does not have to be the same as your local one.

4. Once your new repo is created you should see a screen with instructions about setting it up. Copy the link at the top in the `Quick Setup` section

5. Go back to your Terminal window and enter the following command, replacing the link with the one you copied in the previous step

```bash
    git remote add origin https://github.com/user/repo.git
```

6. To push your local repository to Github execute the following command
   > Note: You will need to provide your Github account details when prompted

```bash
    git push -u origin master
```

7. Once you have executed this command, refresh your repository page on Github, you should now be able to see all the files from your local repo!

# Part C: Local and remote branches

1. In your Terminal, enter the command `git branch`, you should see a list of all your branches, which at the moment is just the default `master`

2. Enter the following command to create a new branch

```bash
    git checkout -b newbranch
```

3. Enter `git branch` to verify that the new branch has been created.

4. Make a change to your `example.txt` file and save it

5. Commit your changes to the new branch by executing the following commands:

```bash
    git add .
    git commit -m "Added more text"
```

6. Push this new branch to Github by executing

```bash
    git push -u origin newbranch
```

7. Refresh your repository page on Github and click on the `branch` dropdown on the left side right above the file list. You should be able to see your new branch and view the changes to the files in your new branch by clicking on it in the dropdown

8. In your Terminal, switch back to the master branch using the following command:

```bash
    git checkout master
```

9. Re-execute steps 4 and 5 on the `master` branch, making sure to change the text to something different than `newbranch`

10. Merge your new two branches into one by executing

```bash
    git merge newbranch
```

> Note: This should cause a [merge conflict](https://help.github.com/articles/resolving-a-merge-conflict-using-the-command-line/), which occurs when the same file has been edited on two different branches with different revisions

11. Open your `example.txt` file and note that it should resemble the following

```
<<<<<< HEAD
...
=======
...
>>>>>> newbranch
```

12. Edit the text file to your choosing and commit the change using

```
    git add .
    git commit -m "Merge newbranch"
    git push
```

13. Refresh your repository github page and you should see these new changes! Scroll down on your profile and you should see a grid with a green square at the end of it to show your activity for today

:tada::tada::tada: You have now completed the QMIND 2018 Git/Github Workflow Tutorial! Go get those green squares.

For further reading, checkout [The Official Github Guides](https://guides.github.com/activities/hello-world/) and make sure to add any projects on your computer to your profile!
