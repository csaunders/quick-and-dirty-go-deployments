# Quick and Dirty Go Application Ansible Playbook

**This is currently still in progress and needs to be actually tested**

These ansible playbooks should help ease the deployment of your Go application. It assumes that your
app server and build server are the same system, but this should be sufficient for hobby or small
projects where deploying your binary to multiple servers isn't as much of a concern.

[Read the article that these playbooks are based off of](http://learningtolearn.sndrs.ca/blog/2015-03-29-quick-and-dirty-guide-to-deploying-go-apps/)


There are two playbooks that you can use:

- Setup: This provisions a server running Ubuntu or Debian to run Monit, Nginx and installs the Go development environment. As a final step it will also deploy your application.
- Deploy: This is just responsible for deploying new code to your server and restarting the application. Ansible playbooks that do the other steps can be slow, so if you know your server is already provisioned you should use this playbook. It assume that the environment was setup as per the `setup` playbook.
