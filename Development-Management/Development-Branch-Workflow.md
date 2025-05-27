## Development Management

### Branch Workflow

The Capstone project uses a `main` and `release-candidate` branch. Any pull requests to either of these branches results in the following actions:

   * pull request to `release-candidate` - deploy to test environment
   * pull request to `main` - deploy to live environment

The class is generally split into two teams so the tasks can be split by front-end and back-end functionality (or by any other categorisation the teams wish to use). Each team member will create a remote branch using their username as a suffix, as show here:

   ![branch-workflow](/.attachments/development-branch-workflow.png)

   *Figure 2 - Branch Workflow Process*

Team members will work on their local branch, pushing to their remote branch often to ensure regular remote backups. Close coordination with team leaders will to reduce the chance of code conflicts when merging units of work to the team branches.

When the team leaders and build managers are ready, pull requests can be issues to push the team branch commits to the `release-candidate` branch.

Once the code from all the team members has been merged and tested, a pull request can be created into the `main` branch.
