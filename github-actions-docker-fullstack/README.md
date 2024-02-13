# GitHubActions pipeline with Flask (backend) and React (frontend) apps

<img src=pic.PNG alt="GitHubActions pipeline">

## Clone project 

```bash
gh repo clone sauravdwivedi/GitHubActions
```

## Setup git repo 
Copy project directory to a git repo and configure that repo in Jenkins pipeline. Docker should be up and running.

## Setup Docker Hub credentials

Install Docker Pipeline plugin in Jenkins, and setup docker hub credentials (Manage Jenkins -> Manage Plugins):

- https://gcore.com/learning/building-docker-images-to-docker-hub-using-jenkins-pipelines/

Modify Jenkinsfile accordingly:

```json
registry = "<Your docker hub username>/<Your repository name>"
```

## Backend and Frontend apps

If GitHubActions pipeline works fine, then backend and frontend apps run on

- http://127.0.0.1:5000/api/v1/ui/
- http://127.0.0.1:3000

## GitHubActions console output

<img src=log.PNG alt="Jenkins log">