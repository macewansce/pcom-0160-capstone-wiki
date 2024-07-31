## Development Management

### The Git Workflow

The Capstone project uses a remote source repository hosted in Azure DevOps Repo. The repository contains the web and web-api code along with settings and documentation.

You will be using Visual Studio and Visual Studio Code to manage your work, and they both have full git support and Azure DevOps integration.

Even though all source management tasks can be done using menu options in each application it is a good idea to review what the git workflow process is:

   ![git-workflow](/.attachments/development-git-workflow.png)

   Figure 1 - Git Workflow Process

The general workflow when coding is:

   * Clone your starting repository
   * Make changes to code and other artifacts
   * Add changes to the staging area
   * When you have a unit of work ready, commit your changes to your local branch
   * Before the end of your working session:
	 * Pull from your remote branch
     * Push your changes to your remote branch

Once you have established your local branch, always remember to pull then push (or sync, in the Visual Studio world).


### Branch Workflow

The Capstone project uses a `main` and `release-candidate` branch. Any pull requests to either of these branches results in the following actions:

   * release-candidate - deploy to test environment
   * main - deploy to live environment

The class is generally split into two teams so the tasks can be split by front-end and back-end functionality. Each team member will create a remote branch using their username as a suffix, as show here:

   ![branch-workflow](/.attachments/development-branch-workflow.png)

   Figure 2 - Branch Workflow Process

Team members will work on their local branch, pushing to their remote branch often to ensure regular remote backups. Close coordination with team leaders will to reduce the chance of code conflicts when merging units of work to the `team` branches.

When the team leaders and build managers are ready, pull requests can be issues to push the team branch commits to the `release-candidate` branch.

Once the code from all the team members has been merged and tested, a pull request can be created into the `main` branch.


### Branch Strategy

This branch strategy may appear complicated but after using it for a week or two it will become second nature.

   ![branch-strategy](/.attachments/development-branch-strategy.png)

   Figure 3 - Branch Strategy Process

The `main` branch represents the code deployed to the live environment.

The `release-candidate` branch holds code deployed to the test environment.

Each team will have a branch for their code. Here is an example scenario:

   * Team 1 is working on the front-end Angular project
      * A `team1` remote branch is created from `release-candidate` on Azure DevOps
      * Each team member creates a `team1-profilename` remote branch from the `team1` branch
      * Team 1 userX has a branch `team1-userX` and they add the category list elements to the code
      * The category page is tested successfully and a pull request is issued to merge `team1-userX` into `team1`
      * Because the work can be used by the back-end team, a pull request is issues to merge `team1` into `release-candidate`
      * The code is then pushed to `main`, and the merged code is refreshed back into `release-candidate` and the two team branches

The important thing to remember is to pull from either `release-candidate` or `main` after a merge from your team.
