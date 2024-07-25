# Development Management

## The Git Workflow

The Capstone project uses a remote source repository hosted in Azure DevOps Repo. The repository contains the web and web-api code along with settings and documentation.

You will be using Visual Studio and Visual Studio Code to manage your work, and they both have full git support and Azure DevOps integration.

Even though all source management tasks can be done using menu options in each application it is a good idea to review what the git workflow process is:

![git-workflow.png](/.attachments/git-workflow.png)
Figure 1 - Git Workflow Process

The general workflow when coding is:

   * Clone your starting repository
   * Make changes to code and other artifacts
   * Add changes to the staging area
   * When you have a unit of work ready, commit your changes to your local branch
   * Before the end of your session:
	 * Pull from your remote branch
     * Push your changes to your remote branch

Once you have established your local branch, always remembr to pull then push (or sync, in the Visual Studio world).


## Branch Workflow

The Capstone project uses a `main` and `release-candidate` branch. Any pull requests to either of these branches results in the following actions:
   * main - deploy to live environment
   * release-candidate - deploy to test environment

The class is usually split into two teams so the tasks can be split by front end and back end functionality. Each team member will create a remote branch using their username as a suffix, as show here:

![branch-workflow.png](/.attachments/branch-workflow.png)
Figure 2 - Branch Workflow Process

Team members will work on their local branch, pushing regularly to ensure regular remote backups. Close coordination with team leaders will to reduce the chance of code conflicts when merging units of work to the team branches.

When the team leaders and build managers are ready, pull requests can be issues to push the team branch commits to the release-candidate branch.


## Branch Strategy

This branch strategy may appear complicated but after using it for a week or two it will become second nature.

![branch-strategy.png](/.attachments/branch-strategy.png)
Figure 3 - Branch Strategy Process

The important thing to remember is to pull from either `release-candidate` or `master` after a merge from your team.
