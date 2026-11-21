# ep_pad-lister2

[![npm version](https://img.shields.io/npm/v/ep_pad-lister2)](https://www.npmjs.com/package/ep_pad-lister2)

A pad overview plugin for Etherpad 3.x. Adds a link to the Etherpad
home page and provides a separate page listing pads by their last edit.

This project continues development of
[ep_pad-lister](https://github.com/ktt-ol/ep_pad-lister), whose upstream
repository has been archived.

## Features

- Lists pads with their revision number and last edit date.
- Displays custom pad titles from
  [ep_set_title_on_pad](https://github.com/ether/ep_set_title_on_pad),
  with compatibility fixed for Etherpad 3.x.
- Excludes pads without any changes and pads whose names start with `private_`.
- Includes translations for English, German, Spanish, French, Italian,
  Dutch, Polish, Brazilian Portuguese, Turkish and Ukrainian.
- Supports Colibris dark mode on the home page link box and the pad overview.

## Requirements

Developed for Etherpad 3.x and manually tested with Etherpad 3.3.19
using the Colibris skin.

## Installation

From your Etherpad directory, run:

```sh
pnpm run plugins install ep_pad-lister2
```

Restart Etherpad after installation. Open its home page and follow
the Padlist link, or visit `/pad-lister`.

### Installing from a local checkout

For development or testing, install a local checkout from your
Etherpad directory:

```sh
pnpm run plugins install --path /path/to/ep_pad-lister2
```

Restart Etherpad after installation.

## Migrating from ep_pad-lister

Replace `ep_pad-lister` with `ep_pad-lister2` in your plugin installation
or container build. Install one version of the plugin at a time.

The `/pad-lister` URL and the `private_` prefix are retained.
No pad data migration is required, and the plugin needs no dedicated
configuration block in `settings.json`.

## Appearance and dark mode

The pad overview loads the active Etherpad skin's home page stylesheet.
Its appearance therefore depends on the selected skin. Dark mode has
been tested with Colibris on Etherpad 3.3.19.

Dark mode follows Etherpad's global `enableDarkMode` setting in
`settings.json`, which is enabled by default. The plugin requires
no separate configuration.

When enabled, the overview follows the browser's color scheme and
updates without reloading. A light-mode preference saved in a pad
on the same origin takes precedence.

## Credits

Based on ep_pad-lister by Holger Cremer and its contributors.
