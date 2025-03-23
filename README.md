# Obsidian Sample Plugin

This is a sample plugin for Obsidian (https://obsidian.md).

## Features

This template demonstrates basic functionality that the Obsidian plugin API offers:

- Adds a ribbon icon
- Adds a command to open a modal
- Adds a plugin settings tab
- Registers global events (click and interval)

## For Plugin Developers

### Quick Start

1. Clone this repository to a local development folder.
2. Install NodeJS (version 16 or higher).
3. Run `npm i` in the command line under your repo folder to install dependencies.
4. Run `npm run dev` to start compilation in watch mode.
5. Create a symlink to "install" the plugin in your Sandbox vault: `ln -s "$(pwd)/dist" /path/to/sandbox/.obsidian/plugins/my-plugin`

### Development Workflow

1. Make changes to `src/main.ts` (or create new `.ts` files in the `src` folder).
2. Those changes should be automatically compiled into the `dist` folder.
3. Reload Obsidian to load the new version of your plugin.
4. Enable the plugin in Obsidian's settings window.

### Releasing New Versions

1. Update `manifest.json` with your new version number and the minimum Obsidian version required.
2. Update `versions.json` with `"new-plugin-version": "minimum-obsidian-version"`.
3. Create a new GitHub release using your new version number as the "Tag version".
4. Upload the files from the `dist` folder as binary attachments to the release.
5. Publish the release.

> You can use `npm version [patch|minor|major]` to simplify the version bump process.

### Adding Your Plugin to the Community Plugin List

This template already comes with a GitHub action that generates a new GitHub release when you add a new tag to the repo.

1. Check the [plugin guidelines](https://docs.obsidian.md/Plugins/Releasing/Plugin+guidelines).
2. Publish an initial version.
3. Ensure you have a `README.md` file in the root of your repo.
4. Make a pull request at https://github.com/obsidianmd/obsidian-releases to add your plugin.

## Improve code quality with eslint (optional)

[ESLint](https://eslint.org/) is a tool that analyzes your code to quickly find problems and suggest improvements.

1. Install ESLint:
   ```bash
   npm install -g eslint
   ```

2. Analyze the project:
   ```bash
   eslint src/**/*.ts
   ```

This command will analyze all TypeScript files in the `src` folder and its subfolders, providing a report with suggestions for code improvement by file and line number.

For more detailed configuration, you can make changes to the `.eslintrc.js` file in the project root.

## Funding URL

You can include funding URLs where people who use your plugin can financially support it.

The simple way is to set the `fundingUrl` field to your link in your `manifest.json` file:

```json
{
	"fundingUrl": "https://buymeacoffee.com"
}
```

If you have multiple URLs, you can also do:

```json
{
	"fundingUrl": {
		"Buy Me a Coffee": "https://buymeacoffee.com",
		"GitHub Sponsor": "https://github.com/sponsors",
		"Patreon": "https://www.patreon.com/"
	}
}
```

## API Documentation

See https://github.com/obsidianmd/obsidian-api
