This is a GitHub Actions workflow I created that publishes my profile website. Here are the steps I took to accomplish this:
1. Disable automatic GitHub Pages publishing in the repo's settings. This required changing the Pages settings source to 'GitHub Actions'.
2. Setup the GitHub Actions workflow. I created required directories and composed a workflow file in yaml format 'deploy.yml' using previously written code.
3. Test the Workflow. I committed and pushed the changes to the repository. I then checked the workflow in the Actions tab to make sure it completed successfully and then checked the live web pages in a new tab.

The only issue I encountered was disabling Pages. In Part 1 Step 2 of the GitHub Actions assignment, the Source section has the drop down options 'Deploy from a branch' and 'GitHub Actions'. There isn't a 'None' option there. There is a 'None' option in the dropdown under 'Branch' just below it. I first selected 'None' there, but that did not disable Pages. Upon research and confirming with Dave, I discovered the latest version of GitHub's website changed the 'None' option to 'GitHub Actions'. After selecting that, GitHub Pages was disabled.

The following is instructions for how to trigger the deployment:
Go to the GitHub repo's settings and disable automatic page publishing.
Commit changes made in the deploy.yml workflow file and then push the changes to the GitHub repo. This triggers the workflow, which executes the jobs and steps in the deployment workflow. A repository event such as 'push' triggers GitHub workflows as long as the trigger event is enabled in the workflow (on: push:). You can manual re-trigger the deployment by clicking 'rerun all jobs'.
