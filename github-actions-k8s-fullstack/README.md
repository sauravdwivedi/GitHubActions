# GitHubActions pipeline with Flask (backend) and React (frontend) apps

<img src=pic.PNG alt="GitHubActions pipeline">

## Architecture

```mermaid
flowchart LR
    A(runner at host)
    B(git hub actions)
    C(docker registry)
    D(k8s cluster at host)
    A --> |fetch job| B
    B --> |receive job| A
    A --> |push image| C
    C --> |pull image| A
    A --> |deploy image| D
```

## Clone project 

```bash
gh repo clone sauravdwivedi/GitHubActions
```

## Setup git repo 

Copy project directory to a git repo and configure that repo from Actions tab.

## Setup Docker Hub credentials

In github under Settings > Secrets and variables > actions, create Repository secrets

```yaml
DOCKERHUB_USERNAME: <<username of your docker hub account>>
DOCKERHUB_TOKEN: <<Access token generated from docker hub under My Account > Security > Access Tokens>>
```

## Setup self hosted runner

- https://docs.github.com/en/actions/hosting-your-own-runners/managing-self-hosted-runners/adding-self-hosted-runners

Create alias for self host runner

```bash
alias actions=/Users/sdwivedi/actions-runner/run.sh
```

run actions in terminal for pipeline to pick up the job. Docker and a kubernetes cluster must be up and running on the host.

## Backend and Frontend apps

If GitHubActions pipeline works fine, then backend and frontend apps run on

- http://127.0.0.1:5000/api/v1/ui/
- http://127.0.0.1:3000

## GitHubActions console output

<img src=log.PNG alt="Jenkins log">

## GitHubActions syntax

- https://docs.github.com/en/actions/using-workflows/workflow-syntax-for-github-actions