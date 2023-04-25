# LSP-vale

This is a helper package that automatically installs and updates [`vale-ls`][1] for you. Vale is a syntax-aware linter for prose built with speed and extensibility in mind.

## Requirements

To use this package, you must have the [LSP][3] package installed.

> It's recommended, but not required, to install the [LSP-json][2] package which will provide auto-completion and validation for this package's settings.

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