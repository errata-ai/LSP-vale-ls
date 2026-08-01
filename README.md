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

The server also provides:

- **Diagnostics**: Vale's alerts, updated as you type rather than only on save (see `lintOnChange` and `debounceMs`).
- **CodeLensProvider**: a per-document metrics lens — word count, reading time, and so on (see `showMetrics`).
- **Vocabulary code actions**: accept a flagged term into your vocabulary, or reject it.

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
                    "initialization_options": {
                        // Put your settings here
                    }
                }
            }
        }
    }
    ```

### Settings

| Setting | Default | Description |
| --- | --- | --- |
| `installVale` | `true` | Install and update Vale automatically. If `false`, Vale must be installed and available on your `$PATH`. |
| `syncOnStartup` | `true` | Run `vale sync` when the server starts. |
| `filter` | `""` | An [output filter][5] to apply when calling Vale. |
| `configPath` | `""` | An absolute path to a `.vale.ini` file, used instead of the default search process. |
| `valeBinaryPath` | `""` | An absolute path to the Vale binary to run, instead of the server-managed copy. |
| `lintOnChange` | `true` | Lint the buffer as it changes, not just when it's saved. |
| `debounceMs` | `300` | How long typing has to settle before linting, in milliseconds. |
| `showMetrics` | `true` | Show the document metrics code lens. |
| `root` | `""` | An absolute path to the directory to run Vale from, instead of the document's workspace folder. |

### Commands

From the Command Palette:

- `LSP-vale-ls: Sync Configuration` — download the packages and styles your `.vale.ini` asks for.
- `LSP-vale-ls: Install or Update Vale` — install or update the server-managed copy of Vale.

[1]: https://github.com/vale-cli/vale-ls
[2]: https://packages.sublimetext.io/packages/LSP-json
[3]: https://packages.sublimetext.io/packages/LSP
[4]: https://www.sublimetext.com
[5]: https://vale.sh/manual/filter/
