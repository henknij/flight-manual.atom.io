---
title: Atom Packages
---
### Atom Packages

First we'll start with the Atom package system. As we mentioned previously, Atom itself is a very basic core of functionality that ships with a number of useful packages that add new features like the [Tree View](https://github.com/atom/tree-view) and the [Settings View](https://github.com/atom/settings-view).

In fact, there are more than 70 packages that comprise all of the functionality that is available in Atom by default. For example, the [Welcome dialog](https://github.com/atom/welcome) that you see when you first start Atom, the [spell checker](https://github.com/atom/spell-check), the [themes](https://github.com/atom/one-dark-ui) and the [fuzzy finder](https://github.com/atom/fuzzy-finder) are all packages that are separately maintained and all use the same APIs that you have access to, as we'll see in great detail in link:/hacking-atom[Hacking Atom].

This means that packages can be incredibly powerful and can change everything from the very look and feel of the entire interface to the basic operation of even core functionality.

In order to install a new package, you can use the Install tab in the now familiar Settings view. Simply open up the Settings view (`cmd-,`), click on the "Install" tab and type your search query into the box under Install Packages that hints "Search Packages".

The packages listed here have been published to [atom.io](https://atom.io/packages) which is the official registry for Atom packages. Searching on the settings pane will go to the atom.io package registry and pull in anything that matches your search terms.

![Package install screen](../../images/packages-install.png)

All of the packages will come up with an "Install" button. Clicking that will download the package and install it. Your editor will now have the functionality that the package provides.

#### Package Settings

Once a package is installed in Atom, it will show up in the side pane under the "Packages" tab, along with all the preinstalled packages that come with Atom. To filter the list in order to find one, you can type into the "Filter packages by name" textbox.

![Package settings screen](../../images/package-specific-settings.png)

Clicking on the "Settings" button for a package will give you the settings screen for that package specifically. Here you have the option of changing some of the default variables for the package, seeing what all the command keybindings are, disabling the package temporarily, looking at the source code, seeing the current version of the package, reporting issues and uninstalling the package.

If a new version of any of your packages is released, Atom will automatically detect it and you can upgrade the package from either this screen or from the "Updates" tab. This helps you easily keep all your installed packages up to date.

#### Atom Themes

You can also find and install new themes for Atom from the Settings view. These can be either UI themes or syntax highlighting themes and you can search for them from the "Install" tab, just like searching for new packages. Make sure to press the "Themes" toggle next to the search box.

![Theme search screen](../../images/themes.png)

Clicking on the theme title will take you to a profile page for the theme on atom.io, which usually has a screenshot of the theme. This way you can see what it looks like before installing it.

Clicking on "Install" will install the theme and make it available in the Theme dropdowns as we saw in [Color Themes](/getting-started/sections/atom-basics/#changing-the-theme).

![Example of the Unity UI theme with Monokai syntax theme](../../images/unity-theme.png)

#### Command Line

You can also install packages or themes from the command line using `apm`.

Check that you have `apm` installed by running the following command in your terminal:

```shell
$ apm help install
```

You should see a message print out with details about the `apm install` command.

If you do not, launch Atom and run the _Atom > Install Shell Commands_ menu to install the `apm` and `atom` commands.

You can also install packages by using the `apm install` command:

* `apm install <package_name>` to install the latest version.
* `apm install <package_name>@<package_version>` to install a specific version.

For example `apm install emmet@0.1.5` installs the `0.1.5` release of the [Emmet](https://github.com/atom/emmet) package.

You can also use `apm` to find new packages to install. If you run `apm search`, you can search the package registry for a search term.

```
$ apm search coffee
Search Results For 'coffee' (5)
├── coffee-trace Add smart trace statements to coffee files with one keypress each. (77 downloads, 3 stars)
├── coffee-navigator Code navigation panel for Coffee Script (557 downloads, 8 stars)
├── atom-compile-coffee This Atom.io Package compiles .coffee Files on save to .js files. (myJavascript.coffee -> myJavascript.js) (349 downloads, 4 stars)
├── coffee-lint CoffeeScript linter (3336 downloads, 18 stars)
└── git-grep `git grep` in atom editor (1224 downloads, 9 stars)
```

You can use `apm view` to see more information about a specific package.

```
$ apm view git-grep
git-grep
├── 0.7.0
├── git://github.com/mizchi/atom-git-grep
├── `git grep` in atom editor
├── 1224 downloads
└── 9 stars

Run `apm install git-grep` to install this package.
```
