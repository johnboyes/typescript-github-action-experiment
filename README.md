# typescript-github-action-experiment

A minimal GitHub Action experiment testing whether Node 24 can execute a
TypeScript entry point directly, without a build step, bundler, or runtime
dependencies.

The `end_to_end` workflow invokes the local action on an Ubuntu GitHub-hosted
runner. Its result is the experiment's validation: the action should execute
`index.ts` and print `Hello World`.
