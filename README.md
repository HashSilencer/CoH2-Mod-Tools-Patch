# CoH2 Mod Tools Patch

A drop-in patch for the **Company of Heroes 2 Tools** (Attribute Editor and ModBuilder):

- **Bug fixes**: no more scroll jumping to the top, no crash when another program holds the clipboard,
  base-game text shown when the editor is started directly, Ctrl+V pastes into every selected value,
  no crash after canceling a ModBuilder build or refreshing Find References after a delete.
- **Safer delete**: references are moved to another instance (or the base-game original) before deleting,
  and both steps can be undone.
- **Themes**: Classic, Light and Dark.
- **DPS Site Editor** (Plugins menu): build a DPS comparison website for your mod from its own data.
- **Agent access**: an AI agent (Claude, Codex, OpenClaw, ...) can read and edit the open Attribute Editor
  through MCP, **only after you click Yes**. Every change is a normal Undo step and nothing is ever saved for you.
- **Updated base-game stats**: the official tools stopped at the April 22nd 2020 hotfix; this brings the
  editor's game data up to the current game.

## Download

Get the zip from [Releases](../../releases/latest).

## Install

1. Close the Attribute Editor and ModBuilder.
2. Read `_readme_For_Update_Attribute_Editor_Stats.md` in the zip and delete the instances it lists from
   your tools' `assets\data\attributes\instances` (the game no longer has them).
3. Copy everything in the `CoH2 Mod Tools Patch` folder into your tools folder, overwriting when asked:
   `...\Steam\steamapps\common\Company of Heroes 2 Tools\`
4. Open your mod in ModBuilder and open Attributes as usual. You should see a **Plugins** and an **Agent**
   menu at the right end of the menu bar.

The full guide (every change, the DPS Site Editor, connecting an agent, and a reference written for
agents) is `_readme_CoH2_Mod_Tools_Patch.md` in the zip.

To uninstall: Steam → Company of Heroes 2 Tools → Properties → Installed Files → **Verify integrity of
tool files**.

## Notes

- `AttributeEditorXML.exe` and `ModBuilder.exe` are Relic's tools with bug fixes applied; Company of Heroes 2
  and its tools belong to Relic Entertainment / SEGA. This is an unofficial community patch.
- The Light / Dark themes use [AdonisUI](https://github.com/benruehl/adonis-ui) (MIT, license included in the zip).
- Agent access listens on your own computer only (127.0.0.1).
