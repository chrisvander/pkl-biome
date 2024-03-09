# pkl-biome

A [Pkl](https://pkl-lang.org) module for [Biome.js](https://biomejs.dev) configuration.

## Usage

You can amend this package's provided module to configure Biome.js. Simply add the following line to a Pkl file (name doesn't matter, but `biome.pkl` makes sense) in your project:
```pkl
amends "package://pkg.pkl-lang.org/github.com/chrisvander/pkl-biome/pkl-biome@1.6.0#/BiomeDefault.pkl"
```

and then specify your configuration below. With the VSCode Pkl extension, you'll get autocomplete for all the available options.

You can change the file name from `BiomeDefault.pkl` to `BiomeGit.pkl` if you want a Biome.js configuration with boilerplate Git support.

To build, run `pkl eval biome.pkl -m .`

## Development

This project uses [Mise](https://mise.jdx.dev) to handle dependencies. To install all dependencies, run `mise install`, followed by `pnpm i`.

## Release Flow

This module tracks with the version of Biome.js it supports. When a new version of Biome.js is released, a new version of this module is released as well. A GitHub Action, on a cron schedule, checks for new versions of Biome.js and triggers creation of a new version PR when it finds a difference. The PR is then merged by a maintainer.
