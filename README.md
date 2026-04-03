# CE Reviewers & Orchestrators

Default reviewer personas and orchestrator definitions for the [Compound Engineering](https://github.com/EveryInc/compound-engineering-plugin) Claude Code plugin.

## Usage

Add this repo as a source in your config files:

```yaml
# ~/.config/compound-engineering/reviewer-sources.yaml
sources:
  - name: ce-default
    repo: JumpstartLab/ce-reviewers
    branch: main
    path: reviewers

# ~/.config/compound-engineering/orchestrator-sources.yaml
sources:
  - name: ce-default
    repo: JumpstartLab/ce-reviewers
    branch: main
    path: orchestrators
```

Then run `/ce:refresh` to sync.

## Reviewers

Each `.md` file in `reviewers/` is a self-contained reviewer persona with frontmatter (name, description, model, tools) and a prompt body defining the reviewer's focus, confidence calibration, and output format.

## Orchestrators

Each `.md` file in `orchestrators/` defines a workflow — which phases to execute, which reviewers to prioritize, and how to synthesize findings. Invoke with `/ce:run <name>`.

| Orchestrator | Style |
|---|---|
| **LFG** | Standard pipeline — plan, work, review, ship. No shortcuts. |

## Adding your own

Fork this repo and add your own `.md` files to `reviewers/` or `orchestrators/`. See any existing file for the format. Point your source config at your fork.
