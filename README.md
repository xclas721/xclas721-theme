# xclas721-theme

A dark teal app theme for Orca, with matching code and terminal colors.

- `themes/dark.json`: app colors (`tokens`) and code colors (`tokenColors`).
- `terminal/dark.json`: terminal ANSI palette.

## Develop

```sh
orca plugin validate .
orca plugin dev watch .    # loads this folder into Orca and reloads on save; Ctrl-C unloads it
```

## Install

```sh
orca plugin install <path to this folder>
```

## License

MIT. See `LICENSE`.
