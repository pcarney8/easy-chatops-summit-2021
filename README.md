# Easy ChatOps based Release Automation with Tekton, ArgoCD and GitHub Actions

## Prerequisites
1. An OpenShift cluster, with credentials stored as GitHub Repository Secrets
  - `OPENSHIFT_PASSWORD`
  - `OPENSHIFT_SERVER`
  - `REGISTRY_PASSWORD`
  - `REGISTRY_USER`
  - `SLASH_TOKEN`
1. ArgoCD deployed
1. Tekton deployed

## How everything works

Tekton is building in the cluster based off of any changes to the xxx directory

- https://github.com/redhat-actions/podman-login
- https://github.com/redhat-actions/openshift-tools-installer
- https://github.com/peter-evans/slash-command-dispatch
- https://github.blog/2020-09-17-github-action-hero-stefan-zweifel-and-git-auto-commit/

Need links for:
- peterjgrainger/action-create-branch@v1.0.0
- mikefarah/yq@3.3.2
- instrumenta/kubeval-action@master
- peter-evans/close-issue@v1
- peter-evans/create-or-update-comment@v1
- stefanzweifel/git-auto-commit-action@v4
- stackrox/kube-linter-action@v1.0.0

Tasks are from:
https://hub-preview.tekton.dev/


