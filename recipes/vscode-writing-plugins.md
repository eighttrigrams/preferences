# Writing Plugins for VSCode

Use "Developer: Reload Window" on each iteration to check your changes. The awesome thing is that even Claude sessions in the terminals continue to work seemlessly after a window reload.

## Local extensions

VSCode can have local extensions at one of two places

1. `~/.vscode/extensions` (global on your system)
2. `your/project/.vscode/extensions` (local to your project)

To install extensions, you would simply need to put them there, or symlink them to there.

If it doesn't install, edit the `extension.json` under `/Users/<username>/.vscode/extensions/`.

```json
{
    "identifier": {
        "id": "eighttrigrams.format-on-save"
    },
    "version": "1.0.0",
    "location": {
        "$mid": 1,
        "path": "/Users/<username>/.vscode/extensions/eighttrigrams.format-on-save-1.0.0",
        "scheme": "file"
    },
    "relativeLocation": "eighttrigrams.format-on-save-1.0.0"
},
```

Alternatively the following should also work

1. Type "Extensions: Install from VSIX..." (command palette)
2. Navigate to this directory and select the extension folder

As always, "Developer: Reload Window" should help (command palette).
