# Updating GitOps repo for Github Action

```yaml
inputs:
  target-option:
    description: |
      string to find target line
      default is 'image'
    required: false
    default: 'image'
  image:
    description: |
      image to update
      required is true
    required: true
  committer-name:
    description: |
      Committer name
      required is false
    required: false
  committer-email:
    description: |
      Committer email address
      required is false
    required: false
  github-token:
    description: |
      Github Token
      required is true
    required: true
  gitops-repo:
    description: |
      GitOps Repo. Must be formatted as <org>/<repo>
      required is true
    required: true
  gitops-repo-path:
    description: |
      Path to clone gitops repository in the workflow
      required is false
      default is 'gitops'
    required: false
    default: 'gitops'
  gitops-repo-ref:
    description: |
      Gitops repo ref to checkout
      required is false
      default is 'main'
    required: false
    default: 'main'
  gitops-repo-file:
    description: |
      GitOps file to update. Please include the file extension and path
      required is false
      default is 'values.yaml'
    required: false
    default: 'values.yaml'
  commit-message:
    description: |
      Commit message to use
      required is false
      default is 'Update GitOps Repo'
    required: false
    default: 'Update GitOps Repo'
  max-retries:
    description: |
      Max retries to commit 
    required: false
    default: 3
```