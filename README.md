# Professional App
[![CircleCI](https://circleci.com/gh/karanchahal/professional-app/tree/master.svg?style=svg)](https://circleci.com/gh/karanchahal/professional-app/tree/master)
This project aims to get you bootstrapped and started as soon as possible with professional git workflows and continous integration and development.

https://circleci.com/gh/karanchahal/professional-app.svg?&style=shield&circle-token=
## Features
 * Docker
 * CircleCI

## Workflow

### Docker

Currently the run command just runs all the tests

1. Build -> ```docker build -t <container-name> . ```
2. Run -> ```docker run -p 3000:3000 <container-name> ```

* Dockerfile gets node image, copies all files in currecnt directory and builds the container

* Building images with tags via versioning ``` docker build -t foo/bar:1.0 ```
* docker-compose.yml is a config file for docker build process, ports, env variables etc
* dockerignore file
* tag git at every release

### Circle CI
 Circle Ci configured under .circleci/config.yml file 

 * On every github event, it builds the docker container and runs it, therby running all the tests

### Git Workflow

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

