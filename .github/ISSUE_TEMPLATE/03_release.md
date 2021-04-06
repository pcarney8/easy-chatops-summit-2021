---
name: Creating a Release
about: A template to use for releasing
title: v1.0.0
labels: ''
assignees: ''

---

## 🤖 Please name this issue what you would like the new release to be called. E.g. "v1.0.0"

The following slash commands are available to use in comments on this issue:

| Command | Description | Parameters |
|---|---|---|
| `/release` | Creates a new tagged release (e.g. v1.0.0), branch (v1.0.0-branch), and Registry image tag (also v1.0.0) based on the current state of the `develop` branch | N/A |
| `/promote` | Promotes with new Registry tag (e.g. demo), updates label ('promoted to demo'), and updates references on branch | N/A |
| `/deploy` | Deploys the promotion to k8s cluster based on Issue Title | `cluster=<ci or prod>`</br>optional: `namespace=<namespace>` note: this is also the name of the `charts/new-app/values-*.yaml` file that will be used |
| `/tekton` | Starts a run of a tekton task or pipeline | `cluster=<ci or prod>`</br>`run=<task or pipeline>`</br>`name=<the name of your task/pipeline>`</br>`namespace=<namespace on kube>`</br>`(optional) branch=<branch name that is different that issue-title-branch>` |
| `/cancel` | Cancels the current release (closes this issue) | N/A |
