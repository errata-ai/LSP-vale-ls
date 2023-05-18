# LSP-vale-ls

This is a helper package that automatically installs and updates [`vale-ls`][1] for [Sublime Text][4]. Vale is a syntax-aware linter for prose built with speed and extensibility in mind.

## Requirements

To use this package, you must have the [LSP][3] package installed.

> It's recommended, but not required, to install the [LSP-json][2] package which will provide auto-completion and validation for this package's settings.

## Features

<table>
    <tr>
        <th>HoverProvider</th>
        <th>CompletionProvider</th>
    </tr>
    <tr>
        <td width="50%">
            <a href="https://user-images.githubusercontent.com/8785025/234143355-c442cbbd-ffc8-445f-a9b8-c3756ac1a5c2.png">
                <img src="https://user-images.githubusercontent.com/8785025/234143355-c442cbbd-ffc8-445f-a9b8-c3756ac1a5c2.png" width="100%">
            </a>
        </td>
        <td width="50%">
            <a href="https://user-images.githubusercontent.com/8785025/234143446-5dcb1f37-7af0-4834-84ca-37bb1db68f1e.png">
                <img src="https://user-images.githubusercontent.com/8785025/234143446-5dcb1f37-7af0-4834-84ca-37bb1db68f1e.png" width="100%">
            </a>
        </td>
    </tr>
    <tr>
        <td width="50%">
          See in-editor documentation for any symbol.
        </td>
        <td width="50%">Autocomplete all <code>StylesPath</code> assets: Styles, Packages, Vocabularies, etc.</td>
    </tr>
    <tr>
        <th>DocumentLinkProvider</th>
        <th>CodeActionProvider</th>
    </tr>
    <tr>
        <td width="50%">
            <a href="https://user-images.githubusercontent.com/8785025/234143624-a6125229-fc74-4051-a40a-92ede8861ab9.png">
                <img src="https://user-images.githubusercontent.com/8785025/234143624-a6125229-fc74-4051-a40a-92ede8861ab9.png" width="100%">
            </a>
        </td>
        <td width="50%">
            <a href="https://user-images.githubusercontent.com/8785025/234143654-d23a42a4-15d3-48cd-95cf-901d9b424b6b.png">
                <img src="https://user-images.githubusercontent.com/8785025/234143654-d23a42a4-15d3-48cd-95cf-901d9b424b6b.png" width="100%">
            </a>
        </td>
    </tr>
    <tr>
        <td width="50%">
          Quickly navigate to external URLs.
        </td>
        <td width="50%">
            Fix alerts with a single click.
        </td>
    </tr>
</table>

## Configuration

There are multiple ways to configure the package and the language server.

- Global configuration: `Preferences > Package Settings > LSP > Servers > LSP-vale-ls`
- Project-specific configuration:
  From the Command Palette run `Project: Edit Project` and add your settings in:

    ```js
    {
        "settings": {
            "LSP": {
                "LSP-vale-ls": {
                    "initializationOptions": {
                        // Put your settings here
                    }
                }
            }
        }
    }
    ```

[1]: https://github.com/errata-ai/vale-ls
[2]: https://packagecontrol.io/packages/LSP-json
[3]: https://packagecontrol.io/packages/LSP
[4]: https://www.sublimetext.com/