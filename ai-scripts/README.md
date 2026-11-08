# ai-scripts

Lua scripts for running Aseprite in batch mode (`aseprite --batch --script <file>.lua`) from AI agents and
command-line pipelines. They are personal tooling kept on the `ai-tools` branch of this fork and are not part of
upstream Aseprite.

Rules:

- Parameters come only from `--script-param key=value` (`app.params`); no dialogs, since there is no UI in batch mode.
- Wrap edits in `app.transaction` and save explicitly with `sprite:saveAs(path)`.
- Work at the game's real size; enlarged images are only previews.

Scripts get added here when the game's art phase needs them (spritesheet export, palette application, preview).
