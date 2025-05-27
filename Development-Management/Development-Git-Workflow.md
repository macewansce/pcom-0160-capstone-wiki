## Development Management

### The Git Workflow

The Capstone project uses a remote source repository hosted in Azure DevOps Repo. The repository contains the web and web-api code along with settings and documentation.

You will be using Visual Studio and Visual Studio Code to manage your work, and they both have full git support and Azure DevOps integration.

Even though all source management tasks can be done using menu options in each application it is a good idea to review what the git workflow process is:

   ![git-workflow](/.attachments/development-git-workflow.png)

   *Figure 1 - Git Workflow Process*

The general workflow when coding is:

   * Clone your starting repository
   * Make changes to code and other artifacts
   * Add changes to the staging area
   * When you have a unit of work ready, commit your changes to your local branch
   * Before the end of your working session:
	 * Pull from your remote branch
     * Push your changes to your remote branch

Once you have established your local branch, always remember to pull then push (or sync, in the Visual Studio world).
