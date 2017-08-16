# Git Together - 8-24-2017

This repo will be the starting point for our demo at the Git Together presentation.

We will aim to demonstrate working with Git in a team, utilizing the command line
and GUI solutions.

# The gameplan

* We'll be building a very basic HTML document with some attached CSS.
* We will demonstrate making a change to the code, committing the change, pushing it to GitHub, making a PR, and merging the PR 
* Along the way, we'll touch on concepts of:
  * Branching
  * Push and Pull
  * Conflicts

## Demo Time
1. Tyler and Francine both login to hangouts and share screens
1. Desktop in meeting room logged in to hangouts
1. Person manning main desktop will toggle presenter screen.

Now we will show the "Hello World" site, and then begin making changes:
1. F - Make a new branch "center". Add centering alignment to elements in #main. Push to GitHub, Create a PR
1. T - Go to GitHub and see the PR, locally pull and test functionality, go back to GitHub and review code changes, and approve PR
1. F - Merge the PR from last step. Pull master. Then create a new branch "francine-feature", change a color in the CSS. Create a PR for this. Explain that we're just going to merge this PR for the demo.
1. T - Create a new branch "tyler-feature", change border-radius to 25px on pixels, and conflicting color change with Francine's above change. Create a PR which should create conflict. Pull master and demo conflict resolution in the GUI.
