# GitHubActions pipeline with Flask (backend) and React (frontend) apps

<img src=pic.PNG alt="GitHubActions pipeline">

## Clone project 

```bash
gh repo clone sauravdwivedi/GitHubActions
```

## Setup git repo 
Copy project directory to a git repo and configure that repo from Actions tab.

## Setup Docker Hub credentials

In github under Settings > Secrets and variables > actions, create Repository secrets:

```yaml
DOCKERHUB_USERNAME: <username of your docker hub account>
DOCKERHUB_TOKEN: <Access token generated from docker hub under My Account > Security > Access Tokens>
```

## Backend and Frontend apps

If GitHubActions pipeline works fine, then backend and frontend apps run on

- http://127.0.0.1:5000/api/v1/ui/
- http://127.0.0.1:3000

## GitHubActions console output

<img src=log.PNG alt="Jenkins log">