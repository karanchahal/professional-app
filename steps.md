# Docker

* Building images with tags via versioning ``` docker build -t foo/bar:1.0 ```
* docker-compose.yml is a config file for docker build process, ports, env variables etc
* dockerignore file
* tag git at every release

# Git 

* git init
* make develop branch , considered to be a brach for all development
* All feature branches (feature/x-feature) is branched out of the develop branch
* Do work commit like usual
* Every feature in unique branches
* Merge back in develop
* Often pull from develop , in your feature branch
* Rebase from develop branch to keep history intact
* After develop has become stable and ready to release, checkout a release branch always prefixed by release/
* Testing on release branch
* Commit directly to release branch , or submit a pull request to the release branch, from a feature / x branch
* After release branch passes testing , it is then merged back into the develop
* Then code from release/x is merged into master, and a github tag is added
* Hot fix branches for emergency fixes to master, branched from master

