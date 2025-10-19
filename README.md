## GitHub Visibility Action

An action which can make the repository it is run in either private or public.


The action takes in a `visibility` parameter which can be either `private` or `public` and a `token`.
The token provided by `token` **MUST** have permission to read and write the repository's administration data.
This is **NOT** possible with the default GitHub action token provided by `GITHUB_TOKEN` and a seperate token must be created and provided through the repository's secrets.

## Creating a Token with administration Access

A toekn with repository administration read and write access is required to use the GitHub visibility action.
To create a token with repository administration access...
1. Click on your GitHub profile picture in the upper right corner.
2. Click on '⚙ Settings'.
3. At the bottom, click 'Developer Settings'.
4. Click on the '🔑 Personal access tokens' dropdown and then click on 'Fine-grained tokens'.
5. Click 'Generate new token'.
6. Fill in the 'Token name' field for your new fine-grained personal access token.
7. Set an expiration for your token. The token will be set to expire after 30 days by default. You can set it to never expire by selecting that option.
8. Set the repository access for your token. Since read and write access to administration data is required, repository access should be as limited as possible.
9. Click '➕ Add permissions' and check the 'Administration' permission.
10. Set the administration permission access to 'Read and write'.
11. Click 'Generate token'.
12. Copy the token to use in the next section.

## Using the Token in a Workflow

1. Go to the repository where you want to use the action and click the '⚙ Settings' tab at the top.
2. Click the 'Secrets and variables' dropdown menu and click 'Actions'.
3. Click 'New repository secret'
4. Name your secret. In this example we'll use `ADMINISTRATION_TOKEN`.
5. Copy the secret from the previous section into the 'Secret' box.
6. Click 'Add secret'.





