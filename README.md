SublimeLinter-contrib-semistandard
================================

[![Build Status](https://travis-ci.org/Flet/SublimeLinter-contrib-semistandard.svg?branch=master)](https://travis-ci.org/Flet/SublimeLinter-contrib-semistandard)

This linter plugin for [SublimeLinter][docs] provides an interface to [semistandard](https://www.npmjs.com/package/semistandard). It will be used with files that have the “javascript” syntax.

## Installation
SublimeLinter 3 must be installed in order to use this plugin. If SublimeLinter 3 is not installed, please follow the instructions [here][installation].

### Linter installation
Before using this plugin, you must ensure that `semistandard` is installed on your system. To install `semistandard`, do the following:

1. Install [Node.js](http://nodejs.org) (and [npm](https://github.com/joyent/node/wiki/Installing-Node.js-via-package-manager) on Linux).

1. Install `semistandard` by typing the following in a terminal:
   ```
   npm install -g semistandard
   ```

1. If you are using `nvm` and `zsh`, ensure that the line to load `nvm` is in `.zshenv` and not `.zshrc`.

1. If you are using `zsh` and `oh-my-zsh`, do not load the `nvm` plugin for `oh-my-zsh`.


**Note:** This plugin requires `semistandard` 2.3.2 or later.

### Linter configuration
In order for `semistandard` to be executed by SublimeLinter, you must ensure that its path is available to SublimeLinter. Before going any further, please read and follow the steps in [“Finding a linter executable”](http://sublimelinter.readthedocs.org/en/latest/troubleshooting.html#finding-a-linter-executable) through “Validating your PATH” in the documentation.

Once you have installed and configured `semistandard`, you can proceed to install the SublimeLinter-contrib-semistandard plugin if it is not yet installed.

### Plugin installation
Please use [Package Control][pc] to install the linter plugin. This will ensure that the plugin will be updated when new versions are available. If you want to install from source so you can modify the source code, you probably know what you are doing so we won’t cover that here.

To install via Package Control, do the following:

1. Within Sublime Text, bring up the [Command Palette][cmd] and type `install`. Among the commands you should see `Package Control: Install Package`. If that command is not highlighted, use the keyboard or mouse to select it. There will be a pause of a few seconds while Package Control fetches the list of available plugins.

1. When the plugin list appears, type `semistandard`. Among the entries you should see `SublimeLinter-contrib-semistandard`. If that entry is not highlighted, use the keyboard or mouse to select it.

## Automatic Formatting
This can be accomplished via @bcomnes StandardFormat on package control.

1) Make sure you have at least `semistandard` version 4.2.2... just update to the latest to be sure:
```bash
npm install semistandard -g
```
2) Install **StandardFormat** from package control
3) Open the "user" package settings for "Standard Format"
  - via command pallete: standard format settings user
  - or via menu: Preference > Package Settings > Standard Format > Settings - User

4) Add a reference to `semistandard -F --stdin`:
```js
{
  // set this to false if you don't want to format on save
  "format_on_save": true,
  "command": ["semistandard", "-F", "--stdin"],
}
```
5) Save the settings file.
6) Restart Sublime Text.

StandardFormat will also map <kbd>CTRL</kbd>+<kbd>ALT</kbd>+<kbd>F</kbd> to format automatically. :)



## Settings
For general information on how SublimeLinter works with settings, please see [Settings][settings]. For information on generic linter settings, please see [Linter Settings][linter-settings].

## Contributing
If you would like to contribute enhancements or fixes, please do the following:

1. Fork the plugin repository.
1. Hack on a separate topic branch created from the latest `master`.
1. Commit and push the topic branch.
1. Make a pull request.
1. Be patient.  ;-)

Please note that modifications should follow these coding guidelines:

- Indent is 4 spaces.
- Code should pass flake8 and pep257 linters.
- Vertical whitespace helps readability, don’t be afraid to use it.
- Please use descriptive variable names, no abbreviations unless they are very well known.

Thank you for helping out!

[docs]: http://sublimelinter.readthedocs.org
[installation]: http://sublimelinter.readthedocs.org/en/latest/installation.html
[locating-executables]: http://sublimelinter.readthedocs.org/en/latest/usage.html#how-linter-executables-are-located
[pc]: https://sublime.wbond.net/installation
[cmd]: http://docs.sublimetext.info/en/sublime-text-3/extensibility/command_palette.html
[settings]: http://sublimelinter.readthedocs.org/en/latest/settings.html
[linter-settings]: http://sublimelinter.readthedocs.org/en/latest/linter_settings.html
[inline-settings]: http://sublimelinter.readthedocs.org/en/latest/settings.html#inline-settings
