# Pipelines: GitHub Actions

This project implements a simple [Continuous Delivery
Pipeline](https://en.wikipedia.org/wiki/Continuous_delivery), based on [GitHub
Actions](https://docs.github.com/en/free-pro-team@latest/actions).

The repository is configured with [GitHub Pages](https://pages.github.com/).
The deployment consists of putting the content of the `main` branch into
`gh-pages` branch which publishes it to the [website](https://slawekzachcial.github.io/pipelines-actions/).

## Spell Check

The pipeline checks the spelling of all markdown files in this repository.

## Link Check

The pipeline checks the links of all markdown files in this repository.

## Git Tag and Release Creation

The pipeline, when run on `main` branch, creates a new Git tag. The tag name is
determined using [Angular Commit Message
Conventions](https://github.com/angular/angular.js/blob/master/DEVELOPERS.md#-git-commit-guidelines).

## Release Deployment

The pipeline, when run on `main` branch, deploys release by copying markdown
files into `gh-pages` branch. The deployment happens only if the markdown files
have been updated. The commit message in `gh-pages` branch contains the release
version number.
