# Publish Skill for Claude Code

A [Claude Code](https://docs.anthropic.com/en/docs/claude-code) skill that automates version bumping and release tagging in a single `/publish` command. Requires the Claude Code CLI, git, and gh (GitHub CLI).

## What's Included

- **SKILL.md** -- The skill definition that drives the `/publish` command. It asks for the version bump type (patch/minor/major), updates the version in the appropriate manifest file(s), commits the change, creates a git tag, pushes to origin, and shows the tag name along with the GitHub Actions runs page. The skill never runs publish commands directly -- publishing is handled by CI via tag-triggered workflows.

## Installation

Clone this repository:

```sh
git clone https://github.com/ai-awesome/skill-publish.git
```

Then install the skill from the local path:

```sh
claude mcp add-skill /path/to/skill-publish
```

Or install directly from the remote URL:

```sh
claude mcp add-skill https://github.com/ai-awesome/skill-publish
```

## Customization

The skill is defined entirely in SKILL.md. Edit it to fit your workflow -- adjust the supported manifest files, change the tagging convention, or modify the post-publish output.

## Contributing

1. Fork this repository and create a feature branch.
2. Make your changes and ensure they are consistent with the existing style.
3. Submit a pull request with a clear description of what you changed and why.
