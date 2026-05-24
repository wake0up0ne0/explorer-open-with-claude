# explorer-open-with-claude

Adds an **Open Claude here** item to the Windows Explorer right-click menu, on the
empty background of a folder. Selecting it opens a terminal in that folder and
starts Claude Code (the CLI) there, so you can drop into Claude in any directory
without typing a path.

## Install

The entry lives in HKLM, so import as administrator:

    reg import open_claude_here.reg

It then shows up when you right-click empty space inside a folder. On Windows 11
with the default menu it is under **Show more options**.

## Remove

    reg import remove_claude_here.reg

## Notes

Paths are hardcoded for this setup:

- Claude Code: `C:\Users\user\.local\bin\claude.exe`
- Icon: `C:\Users\user\.local\bin\claude.ico` (included in this repo)

Edit `open_claude_here.reg` if your paths differ, and copy `claude.ico` to the
icon path above.
