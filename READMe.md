# Creating a Jenkins project and pipeline
## Logging into Jenkins
- Go to [this link](http://35.176.10.123:8080)
- Login using username: `devopslondon`
- Password: `DevopsAdmin`
## Creating a Jenkins project
- On the Jenkins dashboard, click `New Item` found in the top right
- Name the project appropiately and select `Freestyle Project`
- Add a suitable description (Optional)
- Tick the `Discard old builds box` and add `3` under `Max # of builds to keep`. This is to stop unwanted builds from clogging Jenkins
- Under `Build`, click `Add Build step` and select `Execute shell`
- Here, we can add any linux based command. For simplicity, add `uname -a`
- Apply and save the build.
- Now the project can be built by pressing the `Build Now` button or alternatively by right clicking the project on the dashboard]\
## Creating a Jenkins pipeline
- We can create a pipeline to build when the project completes
- Follow the same steps to create a project and add a suitable 'Build step'
- Navigate back to the original project and select `Configure`
- This allows the project to be re-configured when necessary
- For this, scroll down to the bottom and add a new `post-build action`
- Select `Build another project`
- And select the new project.
