# Shell Apps

Create and launch your own shell command shortcuts as apps on Windows, right from Raycast.

## Features

- Create named shortcuts that run any shell command (for example `cliamp`)
- Launch each shortcut in a dedicated terminal window: **PowerShell**, **PowerShell 7**, **Command Prompt**, or **Windows Terminal**
- Optional working directory, keep-window-open, and run-as-administrator (UAC) options
- Turn any shortcut into an app-like **Quicklink** in the root search, and assign it a hotkey
- All data is stored locally on your machine (Raycast's local storage)

## How to use

1. Install the extension from the Raycast Store.
2. Open the **Shell Apps** command.
3. Select **Create Shell App** (or press `⌘` `N`) to add a shortcut:
   - **Name** – the display name, for example `cliamp`.
   - **Command** – the shell command to run, for example `cliamp`.
   - **Terminal** – the terminal used to launch the command.
   - **Working Directory** – optional directory the command runs in.
   - **Keep the terminal window open** – keep the window open after the command exits.
   - **Run as administrator** – launch the terminal elevated (triggers a UAC prompt).
4. Select a shortcut and press `↵` to launch it.

To make a shortcut behave like a real app, select **Create Quicklink**: a named entry appears in the
root search (for example `cliamp`) that launches the command directly. You can also assign it a
hotkey from Raycast's Quicklinks preferences.

## Commands

- **Shell Apps** – manage and launch your shortcuts. When launched with the `app` argument (via a
  Quicklink) it launches the shortcut directly.
- **Create Shell App** – add a new shortcut.

## Troubleshooting

- **The command is not found** – commands are resolved with your user `PATH`. Make sure the tool is
  installed and added to `PATH`, then try again.
- **Windows Terminal unavailable** – the extension automatically falls back to PowerShell when
  `wt.exe` is not installed.
- **Quicklinks created before publishing** – quicklinks created while the extension is in
  development point to the development path. Re-create them after installing the extension from the
  Store.