# Two Truths and a Lie

## Summary

Let's get to know each other better, using Git and GitHub! We'll play an icebreaker called Two Truths and a Lie, but instead of sitting around and chatting in person, we're going to use GitHub to chat about what the lie is.

## Releases

### Release 0: Clone the Repo and Create a Branch

1. Clone this repo. In your browser find the clone URL in the sidebar and copy it. In your terminal, run the following command, replacing `CLONE_URL` with the URL you copied:

  ```shell
  git clone CLONE_URL
  cd two-truths-and-a-lie
  ```

2. Identify your pair:

  ```shell
  git config user.name YOUR_NAME_YOUR_PAIRS_NAME
  ```

  Note that without the `--global` flag this will only affect the current repo, useful if you want to avoid trashing your usual Git config.

3. Now we're going to create a branch! To do this we use the `git branch` command. `git branch` on its own lists out all local branches, but when you give it an argument it creates a new branch. A new branch is a copy of the current branch with a different name.

  In your terminal, run the following command, replacing `YOUR_NAME` with your name:

  ```shell
  git branch YOUR_NAME_YOUR_PAIRS_NAME
  git checkout YOUR_NAME_YOUR_PAIRS_NAME
  ```

  You could also do this in one step:

  ```shell
  git checkout -b YOUR_NAME_YOUR_PAIRS_NAME
  ```

4. Modify the file `two_truths.md` so that for each of you it contains your name, and three facts about you. One of these facts should be completely made up.

5. Add and commit your file to the project with the following commands:

  ```shell
  git add source/
  git commit -m "Added facts about Example McExampleson"
  ```

6. Now push up your branch to GitHub with

  ``` shell
  git push origin YOUR_NAME_YOUR_PAIRS_NAME
  ```
  **DO NOT MERGE YOUR PULL REQUEST IN MASTER!!**

  * Why not? What would happen if everyone merged their branches into master?

### Release 1 : Find the Lie
A teacher will guide you to find the cohort mates with whom you're going to play lie detector. Ask your teacher who you're busting!

1. Pull your cohort mates branch from GitHub into your local repository.

  ```shell
  git fetch
  git checkout THEIR_BRANCH
  ```

2. Create a new branch for your changes

  ```shell
  git checkout -b THEIR_BRANCH-busted
  ```

  * What is the difference between this command and the one in the previous step? 
    * `git --help checkout`

3. Open `two_truths.md` and add the word **LIE** to the line you think is a lie.

4. Add the changed file to your Git staging and commit it.

  ```shell
  git add two_truths.md
  git commit -m "Found the lie"
  ```

5. Push this branch to GitHub

  ```shell
  git push origin THEIR_BRANCH-busted
  ```

6. Submit a pull request on GitHub of your changes.

### Release 2: Come Clean

Now it's time to come clean (or not).

1. Once someone has submitted a LIE pull request on your branch you can comment on the pull request with:

  * "Yep you got it" or
  * "Nope but perhaps you really meant to choose #1" or (if your devious)
  * "Nope, keep guessing".

  In any case, close the pull request and **DO NOT MERGE TO MASTER!! (EVER)**.

## Optimize Your Learning

* Draw a diagram of the Git workflows you used in Release 0 and Release 1.
* Describe the workflow using your picture and words (i.e. not code) to your pair or a teacher.
* Make sure you understand all parts COMPLETELY. You will be using this workfow extensively in the next nine weeks. Ask questions if anything is still unclear!

## Resources

- [My git workflow](workflow.md)
- [GitHub Help](https://help.github.com/)
- [Learn Git Branching](http://pcottle.github.io/learnGitBranching/)
- [Git Cheatsheet](http://byte.kde.org/~zrusin/git/git-cheat-sheet-medium.png)
- [Git homepage](https://git-scm.com/)
- [GitHub Hello World](https://guides.github.com/activities/hello-world/)
- [Gitflow Workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)
