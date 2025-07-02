Invite User and Create Issue Workflow
This GitHub Actions workflow helps you invite a user to the demo-0987 organization and automatically creates an issue in the Invitation-repository once the user accepts the invitation.

How to Use
Make sure you have added a Personal Access Token (PAT) with the following scopes to your repository secrets as GH_PAT:

admin:org

repo

Go to the Actions tab in your repository.

Select the Invite User and Create Issue workflow.

Click Run workflow and fill in the required inputs:

username: GitHub username of the user to invite.

issue_title: The summary/title for the issue to be created.

issue_body: The description/body for the issue.

The workflow will:

Send an invitation to the specified user.

Wait up to 30 minutes for the user to accept the invitation.

Once accepted, automatically create an issue with the provided title and description in the Invitation-repository.

Notes
You need to manually trigger the workflow for each user you want to invite.

If the user does not accept the invitation within 30 minutes, the workflow will fail.

Make sure your GH_PAT secret is kept secure.