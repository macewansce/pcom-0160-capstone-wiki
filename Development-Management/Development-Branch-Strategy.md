## Development Management

### Branch Strategy

This branch strategy may appear complicated but after using it for a week or two it will become second nature.

   ![branch-strategy](/.attachments/development-branch-strategy.png)

   *Figure 3 - Branch Strategy Process*

The `main` branch represents the code deployed to the live environment.

The `release-candidate` branch holds code deployed to the test environment.

Each team will have a branch for their code. Here is an example scenario:

   * Team 1 is working on the front-end Angular project
      * A `team1` remote branch is created from `test` on Azure DevOps
      * Each team member creates a `team1/profilename` remote branch from the `team1` branch
      * Team 1 userX has a branch `team1/userX` and they add the category list elements to the code
      * The category page is tested successfully and a pull request is issued to merge `team1/userX` into `team1`
      * Because the work can be used by the back-end team, a pull request is issues to merge `team1` into `test`
      * The code is then pushed to `main`, and the merged code is refreshed back into `team1` and `team2`

The important thing to remember is to pull from either `test` or `main` after a merge from your team.
