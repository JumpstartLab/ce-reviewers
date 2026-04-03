# CE Reviewers

Default reviewer persona files for the [Compound Engineering](https://github.com/EveryInc/compound-engineering-plugin) Claude Code plugin.

## Usage

Add this repo as a source in your `reviewer-sources.yaml`:

```yaml
sources:
  - name: ce-reviewers
    repo: JumpstartLab/ce-reviewers
    branch: main
    path: reviewers
```

Then run `/ce:refresh` to sync the reviewer files into your plugin.

## Reviewers

Each `.md` file in `reviewers/` is a self-contained reviewer persona with frontmatter (name, description, model, tools) and a prompt body defining the reviewer's focus, confidence calibration, and output format.

## Adding your own

Fork this repo and add your own reviewer `.md` files to `reviewers/`. See any existing reviewer for the format. Point your source config at your fork.
