## AI interaction 1
Date: 9/28/2026
Assistant: UM-gpt
Purpose: AI practice with GitHub
Prompt or summary: I am currently in a class that shows us how to  use git and github. I am doing a lab for the class that is covering github issues. Could you explain what issues are, and how they differ from a branch, commit, and pull request.
Useful suggestion: What is a GitHub issue?
A GitHub issue is a record used to track work or discuss something related to a repository. For example:

A bug that needs fixing
A feature someone wants to add
A task that needs completing
A question or design discussion

An issue can include a title, description, comments, labels, an assignee, and a due date or milestone. GitHub gives each issue a number, such as #42, so it can be referenced elsewhere.
Importantly, an issue describes or tracks work. It does not directly change the project’s files.
How the concepts differ
Branch
A branch is a separate line of development in the Git repository.
You might create a branch for issue #42:
git switch -c fix-login-error
You can change files on this branch without immediately changing the repository’s primary branch, usually named main.
Purpose: Isolate work while you develop or fix something.

Commit
A commit is a saved snapshot of changes in the Git history.
git add .
git commit -m "Validate empty login fields"
Each commit records:

What changed
Who made the change
When it was made
A commit message explaining the change

Purpose: Record a specific set of file changes in Git.

Pull request
A pull request, often abbreviated PR, proposes merging changes from one branch into another.
For example, after making and pushing commits on fix-login-error, you might open a pull request asking to merge that branch into main. Other people can review the code, leave comments, request changes, and approve it.
Purpose: Review, discuss, and merge code changes.
Despite the name, a pull request is primarily a GitHub collaboration feature; it is not the same as running git pull.

Typical workflow
These concepts often fit together like this:

Issue: “Login form crashes when the username is empty” (#42)
Branch: Create fix-login-error to isolate the work.
Commits: Make and save the necessary code changes on that branch.
Pull request: Propose merging fix-login-error into main.
Merge and close: Merge the pull request and close issue #42.

You can connect them by writing something like this in the pull request description:
Closes #42
When the pull request is merged into the repository’s default branch, GitHub can automatically close issue #42.
Quick comparison



Concept
Main purpose
Changes files?



Issue
Track a bug, feature, task, or discussion
No


Branch
Provide an isolated line of development
Holds changes


Commit
Save a snapshot of changes
Yes


Pull request
Propose, review, and merge branch changes
Not by itself; merging applies the commits


A useful mental model is:

Issue = what needs to be doneBranch = where the work is doneCommit = a saved step in the workPull request = a proposal to add the completed work
Decision: accepted
Reason: Simple advice and explanations as to what the differences between each of the subjects are.
Related GitHub URL: https://github.com/cbishop2028/SWE325-Lab8

## AI interaction 2
Date: 9/28/2026
Assistant: UM-gpt
Purpose: AI practice with GitHub
Prompt or summary: Could you review my README.md file and explain some ways that I could make it better and clearer. Here it is: This repository serves the purpose of the home for lab 8 of SWE325. This is a project that teaches us how to use GitHub issues, while using the skills we have already learned throughout the class. Our goal is to use all these things to create a clear, navigable, and easy to understand project.
Useful suggestion: Your README communicates the project’s basic purpose, but you could improve it by making the wording more direct, specific, and organized.
Suggested improvements

Use more natural wording“Serves the purpose of the home for” is wordy. “Contains Lab 8” is simpler.

Clarify what “these things” meansReplace vague phrases with the specific skills or GitHub features being used.

Use active, concise languageFor example, “This lab teaches us” is clearer than “This is a project that teaches us.”

State the learning objectivesBriefly mention what students will practice, such as creating, assigning, labeling, and closing issues.

Add headingsEven a short README is easier to scan with sections such as Overview and Learning Objectives.


Possible revision
# SWE 325 Lab 8: GitHub Issues

## Overview

This repository contains Lab 8 for SWE 325. The lab focuses on using
GitHub Issues to organize, discuss, and track work within a software project.

## Learning Objectives

In this lab, we will:

- Create and manage GitHub issues.
- Write clear issue titles and descriptions.
- Use issues to track project tasks and progress.
- Apply Git and GitHub skills introduced earlier in the course.
- Organize the repository so that it is clear and easy to navigate.
If the lab covers specific features such as labels, milestones, assignees, branches, or pull requests, add those to the objectives rather than claiming them unless they are actually required.
Smaller revision
If you want to keep it as one paragraph:

This repository contains Lab 8 for SWE 325. The lab focuses on using GitHub Issues to organize and track project work while applying Git and GitHub skills introduced earlier in the course. Our goal is to create a project that is clear, easy to understand, and simple to navigate.
Decision: accepted
Reason: I like how it structured the file as a list of things that would be covered.
Related GitHub URL:  https://github.com/cbishop2028/SWE325-Lab8/blob/github-ai-workflow/README.md

## AI interaction 3
Date: 9/28/2026
Assistant: UM-gpt
Purpose: AI practice with GitHub
Prompt or summary: Could you also give me a checklist for a pull-request?
Useful suggestion: You can add this reusable checklist to a pull-request description:
## Pull Request Checklist

### Before submitting

- [ ] I created this pull request from the correct branch.
- [ ] My branch is up to date with the target branch.
- [ ] The pull request has a clear, descriptive title.
- [ ] The description explains what changed and why.
- [ ] I linked the related issue, if applicable (for example, `Closes #12`).
- [ ] I reviewed my own changes.
- [ ] I removed debugging code, unnecessary comments, and unrelated changes.

### Quality checks

- [ ] The project builds or runs successfully.
- [ ] Existing tests pass.
- [ ] I added or updated tests when appropriate.
- [ ] I manually tested the changes.
- [ ] I followed the project’s formatting and style conventions.
- [ ] I updated documentation when necessary.

### Ready for review

- [ ] My commits have clear and meaningful messages.
- [ ] The changes are focused on one task or issue.
- [ ] I added screenshots or examples for visual changes, if applicable.
- [ ] I explained any limitations or known problems.
- [ ] The pull request is ready for review.
For a smaller class assignment, you could use this shorter version:
## Pull Request Checklist

- [ ] The pull request has a clear title and description.
- [ ] The related issue is linked.
- [ ] The changes address the issue's requirements.
- [ ] The code runs correctly.
- [ ] Tests pass, if applicable.
- [ ] Documentation has been updated, if needed.
- [ ] I reviewed my changes before requesting a review.
- [ ] The pull request contains no unrelated changes.
GitHub renders each - [ ] item as an interactive checkbox. A checked item is written as - [x].
Decision: accepted
Reason: The checklist provides a clear and concise way of making sure a pull request is done correctly.
Related GitHub URL: https://github.com/cbishop2028/SWE325-Lab8/blob/github-ai-workflow/workflow-notes.md

Lab 8 reflection questions:

1. Which GitHub action or object was most useful to you, and why?
I think the most useful GitHub action is the pull request because it makes you review your changes before making a huge commitment by merging into the main project.
2. Which AI suggestion did you accept, and what made it useful?
I accepted the AI suggestion to improve the README.md file. This change made the file into a list of things that would be learned/done in the repository. This made the requirements easier to understand.
3. Which AI suggestion did you revise or reject, and why?
I did not revise or reject any of the suggestions. I thought they all improved the repository.
4. What did you verify yourself instead of trusting the AI?
I verified the checklist that it gave me to make sure everything had reasonable requirements. Most of them are things we have already been instructed to do from this class.
5. What would you change in your GitHub workflow next time?
I like how everything went this time. I think the one thing I would change would be adding screenshots just for some form of secondary validation for the AI.
