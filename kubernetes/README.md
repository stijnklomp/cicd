# Kubernetes CI/CD

## Continuous Integration


## Continuous Deployment

### Steps

A. Automatic through commit (Dev env):

1. The user runs a pipeline step that sets the targetRevision to their feature
   branch
	1.a. A confirmation step is required if the targetRevision is NOT currently
	set to point to the main branch. This tries to prevent competing
	simultaneous deployments.
2. Commit to branch

B. Manual (Dev env):

1. The user runs a pipeline stage that sets the targetRevision to a tag that
includes the branch name plus an incrementing ID starting at 0 `<feature branch:0>`
2.

A. Automatic through tag (Dev env):

1. Git tag gets created on main branch (can be done manually or through pipeline
   step)
2. Webhook event

### Setup

A. Automatic

B. Manual:

1. Use `targetRevision` in `Application` manifest to look for `"refs/tags/*"`.