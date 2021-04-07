# Easy ChatOps based Release Automation with Tekton, ArgoCD and GitHub Actions

## Prerequisites
1. An OpenShift cluster, with credentials stored as GitHub Repository Secrets
  - `OPENSHIFT_PASSWORD`
  - `OPENSHIFT_SERVER`
2. ArgoCD deployed and repo added
3. Tekton deployed and Tasks + Pipelines deployed
4. [Personal Access Token](https://docs.github.com/en/github/authenticating-to-github/creating-a-personal-access-token) configured for [chatops slash commands](https://github.com/peter-evans/slash-command-dispatch#token) and GitHub Repository Secret created named: `SLASH_TOKEN` 

## Notes
This example repo uses the idea of a [trunk based development](https://trunkbaseddevelopment.com/)

## How everything works

Tekton is building in the cluster based off of any changes to the `src` directory via GitHub action `.github/workflows/tekton-build.yaml`

Once you are ready to release, create an Issue (use the [Release Issue template](https://github.com/pcarney8/easy-chatops-summit-2021/issues/new?assignees=&labels=&template=03_release.md&title=v1.0.0) for more documentation)

`/release` to create a tagged release based on the name</br>
`/promote` to change the appropriate ArgoCD configs to point the new tag</br>
`/deploy` to deploy via ArgoCD `Application` documentation [here](https://argoproj.github.io/argo-cd/getting_started/#6-create-an-application-from-a-git-repository)

## GitHub Actions are from:
- https://github.com/peter-evans/slash-command-dispatch
- https://github.com/redhat-actions/openshift-tools-installer
- https://github.com/redhat-actions/oc-login
- https://github.com/mikefarah/yq
- https://github.com/peter-evans/close-issue
- https://github.com/peter-evans/create-or-update-comment
- https://github.com/peterjgrainger/action-create-branch
- https://github.com/stefanzweifel/git-auto-commit-action 

## Tekton Tasks & Pipelines are from:

- https://hub.tekton.dev/tekton/task/s2i
- https://hub.tekton.dev/tekton/task/git-clone


