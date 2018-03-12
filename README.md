# PhpStorm IDE configuration

[![PhpStorm version](https://img.shields.io/badge/PhpStorm-2017.3-brightgreen.svg)](https://www.jetbrains.com/phpstorm/)
[![License](https://img.shields.io/github/license/ph-il/phpstorm-config.svg)](https://github.com/ph-il/phpstorm-config/blob/master/LICENSE)

This is my global configuration for [PhpStorm](https://www.jetbrains.com/phpstorm/), my favorite IDE for PHP. I have some custom configuration for code styling, inspections and file templates, and I use
Git to track these configuration files and to synchronize them between workstations. The code style rules are based on [PSR-1](https://www.php-fig.org/psr/psr-1/), [PSR-2](https://www.php-fig.org/psr/psr-2/) and [PSR-12](https://github.com/php-fig/fig-standards/blob/master/proposed/extended-coding-style-guide.md) (which is still a proposal) but I also added some things that are not specified in the PSR guidelines.

Base on [Nic Wortel phpstorm-ide-config](https://github.com/nicwortel/phpstorm-ide-config)

Feel free to use or fork this repository. Note that I use PhpStorm 2017.3. I cannot guarantee compatibility with other versions of PhpStorm.

## Plugin we use

Some configuration is specifically for the [Php Inspections (EA Extended)](https://github.com/kalessil/phpinspectionsea) plugin. I guess this is ignored when you don't have the plugin.

* .env files support
* .ignore
* deep-assoc-completion
* EditorConfig
* PHP Annotations
* PHP Class Templates
* PHP composer.json support
* PHP inheritDoc helper
* Php Inspections (EA Extended)
* PHP Toolbox
* PhpMetrics
* PHPUnit code coverage
* PHPUnit Enhancement
* String Manipulation
* Symfony Plugin

If you use 
* SensioLabsInsight

## Code style settings overview

Language          | Standards
------------------|---------
PHP               | [PSR-1](https://www.php-fig.org/psr/psr-1/), [PSR-2](http://www.php-fig.org/psr/psr-2/), [PSR-12](https://github.com/php-fig/fig-standards/blob/master/proposed/extended-coding-style-guide.md)
HTML / Twig       | 4 spaces
CSS / SCSS / LESS | 2 spaces
Yaml              | 2 spaces

## Installation

Before you do this, make sure PhpStorm is not running, or it will overwrite the changed files before shutting down.

Use the following commands to go to the config directory, remove some default directories, and pull the files from my repository:

```bash
# replace with the actual directory name, depending on OS and PhpStorm version (see below).
cd ~/.PhpStorm2017.3/config

# remove the files and folders that are in this repository
rm -r codestyles/
rm -r fileTemplates/
rm -r inspection/

git init
git remote add origin git@github.com:nicwortel/phpstorm-ide-config.git
git fetch
git checkout -t origin/master
```

### Location of the config folder

OS | Location
---|---------
Windows | `C:\Users\<User name>\.PhpStorm2017.3\config`
Linux | `~/.PhpStorm2017.3/config`
OS X | `~/Library/Preferences/PhpStorm2017.3`

See [Project and IDE settings](https://www.jetbrains.com/phpstorm/help/project-and-ide-settings.html#d739736e149) for more information about the configuration directory structure.

### Subdirectories of the config folder

Directory | Contents
----------|---------
codestyles | Code Style settings (Editor > Code Style)
colors | Colors & Fonts settings (Editor > Colors & Fonts)
fileTemplates | File and Code Templates (Editor > File and Code Templates)
filetypes | File Types (Editor > File Types)
inspection | Inspection profiles (Editor > Inspections)
keymaps | Keyboard shortcuts (Keymap)
templates | Live templates (Editor > Live Templates)
