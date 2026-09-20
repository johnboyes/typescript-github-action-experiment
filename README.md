# typescript-github-action-experiment

A minimal GitHub Action experiment testing whether Node 24 can execute a
TypeScript entry point directly, without a build step, bundler, or runtime
dependencies.

The `end_to_end` workflow invokes the local action on an Ubuntu GitHub-hosted
runner. Its result is the experiment's validation: the action should execute
`index.ts` and print `Hello World`.

The `remote_consumption` workflow invokes the existing `v0.0.4` semantic
version tag remotely:

```yaml
uses: johnboyes/typescript-github-action-experiment@v0.0.4
```

This verifies that the tagged repository contents are sufficient for remote
consumption on a GitHub-hosted runner, without a separately published build or
bundle artifact.
