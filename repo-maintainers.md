# Copilot Workspace for Repository Maintainers

Copilot Workspace can assist you as a repository maintainer in several ways:

1. Copilot Workspace can help you explore potential solutions to issues.
2. Copilot Workspace can help you generate sketches of solutions to issues for potential contributors, lowering the barrier of entry.
3. Copilot Workspace can help encourage a culture where issue-creators leave additional helpful notes on how to solve issues, for use by both contributors and AI assistants.

For example, when a new issue is filed in your repository, you can use Copilot Workspace to generate a sketch of a solution to the issue. You can then use the "Share" button to publish this sketch back to the issue thread, with additional comments about whether you think it is useful or not, and where it might need improvement. This can help potential contributors understand the problem better and provide a starting point for their work.

Similarly, when a new issue is filed, you can ask the contributor to create a Copilot Workspace session for the issue. This may help the contributor understand the problem better and provide a starting point for their work. You can also include this guidance in the issue template for your repository, assuming your users have access to Copilot Workspace. You can also ask contributors to leave additional notes in the Copilot Workspace session, which can help future contributors and AI assistants understand the problem better.

## Restricting the use of Copilot Workspace in your repository

It is possible for undisciplined contributors to over-use AI-assisted code generation. Because of this, we give repository maintainers the option of disabling the direct use of Copilot Workspaces for creating pull requests and/or issue comments in their repositories.

To disable the direct creation of pull requests using Copilot Workspace, create a file `.github/copilot-workspace/policy.json` in the default branch of the repository containing the following content:

```json
{
  "allowPullRequests": false
}
```

To disable the use of Copilot Workspace to directly generate issue comments that contain links to Copilot Workspace sessions, add the following content to the `policy.json` file:

```json
{
  "allowComments": false
}
```

Users of Copilot Workspace will still be able to:

- create sharing links to Copilot Workspace sessions and paste them into issue comments
- push to new branches in your repository (if they have write access)
- push to new branches in forks of your repository
- manually create pull requests from branches
- use Copilot Workspace to generate code snippets and files for their own use in their own pull requests and issue comments to your repository
