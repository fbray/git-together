# Git Together - 8-24-2017

This repo will be the starting point for our demo at the Git Together presentation.

We will aim to demonstrate working with Git in a team, utilizing the command line
and GUI solutions.

# The Game Plan

* We'll be building a very basic HTML document with some attached CSS.
* We will demonstrate making a change to the code, committing the change, pushing it to GitHub, making a PR, and merging the PR.
* Along the way, we'll touch on concepts of:
  * Branching
  * Push and Pull
  * PR review
  * Merge
  * Conflicts

## Demo Time
1. Tyler and Francine both login to hangouts and share screens
1. Desktop in meeting room logged in to hangouts
1. Person manning main desktop will toggle presenter screen.

Now we will show the "Hello World" site, and then begin making changes:
1. T & F - Clone Repo and view file
   * `git clone git@github.austin.utexas.edu:twf369/8-24-git-together.git git-together`
   * Open file in browser of choice.
1. F - Make a new branch "center".
   * Discuss `git branch center && git checkout center` process
   * `git checkout -b center`
   * Add centering alignment to elements in #main
     ```
     #main {
       text-align: center;
     }
     ```
   * `git add demo.html`
   * `git commit -m "Center text."`
   * Push to GitHub: `git push origin master`
   * Create a PR
1. T - Make a branch "tyler-feature"
   * `git checkout -b tyler-feature`
   * Add a new div within #content with some lorem ipsum text
     ```
     <div id="desc">
       Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
     </div>
     ```
   * `git add demo.html`
   * `git commit -m "Add description."`
   * Go to GitHub to review PR
   * Locally, pull branch: `git fetch && git checkout center`
   * Test functionality:  Reload in browser
   * In GitHub, review code changes, and approve PR
1. F - Merge PR from last step in GitHub.
1. F & T -  Pull master:  `git pull origin master`
1. T - Merge master into your branch
   * `git checkout tyler-feature`
   * `git merge master`
   * Change the border radius to 25px: `border-radius: 25px;`
1. F - Create new hotfix branch
   * `git checkout -b hotfix`
   * Change .color color:  `color: #BF5700;`
   * `git commit -am "Update span color."`
   * Explain that we would follow the same PR review process, but for the sake of the demo, we will manually merge this commit.
   * `git checkout master`
   * `git merge hotfix`
   * `git push origin master`
1. T - In your tyler-feature branch, change .color: `color: #43695B`
   * Commit changes: `git commit -am "Add description and styling."`
   * Push branch to GitHub: `git push origin tyler-feature`
   * Create a PR for your branch in GitHub and note the conflict.
   * Pull master again and merge into your branch
     * `git pull origin master && git merge master`
   * Open in GUI and resolve.
   * Push resolved state back to GitHub:
     * `git commit -am "Fix conflict."`
     * `git push origin tyler-feature`
1. F - Review PR
   * `git fetch && git checkout tyler-feature`
   * Reload browser
   * Review code changes in GitHub
   * Approve PR
1. T - Merge PR in GitHub
   * Update your local repo: `git pull origin master`
