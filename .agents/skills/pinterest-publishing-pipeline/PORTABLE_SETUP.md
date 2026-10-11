# Portable setup

This folder is a Codex Skill. Copy `pinterest-publishing-pipeline` into either:

- `<project>/.agents/skills/` to keep it with a project/repository, or
- `~/.codex/skills/` to make it available across projects on one machine.

After copying it to a new environment:

1. Point the task at the destination product folder; this skill intentionally stores no product root.
2. Configure or confirm the GitHub repository, branch, asset subdirectory, and public raw-image URL base for that environment. The repository currently used by one workspace is not a default for future migrations.
3. Ensure the environment has an approved GitHub authentication method. Do not copy a Deploy Key or token into this package.
4. Confirm the Pinterest board name for a new series when it is not already clear from the user's instructions.
5. Keep Pinterest publishing as a manual user action. This skill prepares the batch and does not publish or schedule Pins.

The skill itself has no machine-specific path or credential dependency. PDF rendering and Git operations use the tools available in the destination Codex environment.
