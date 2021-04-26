inventory-hugo-theme
====================

<!--
    Style rule: one sentence per line please!
    This makes git diffs easier to read. :)
-->

Theme used with UNICEF Open Source Inventory portal.
Forked from Dot, a Hugo theme by ThemeFisher.


## Demo

Coming soon via GitHub Pages.


## Installation

The recommended installation method for an existing Hugo project is with a [git submodule](https://git-scm.com/docs/git-submodule).
First, open a terminal and change directories to a Hugo git repository.
Make sure the `themes/` directory is present in your Hugo project.

Use these commands to add the theme into an existing Hugo site:

```bash
git submodule add git@github.com:unicef/inventory-hugo-theme.git themes/inventory
git commit -sm "Add UNICEF Inventory Hugo theme as a git submodule"
git push
```

### Updating a submodule to latest upstream

Alternatively, you may occasionally wish to update your submodule for new changes added upstream.
To pull newer upstream changes into your pre-existing git submodule, run the following from your Hugo project root directory:

```bash
git submodule update --remote --rebase
```

### Contributing

If you want to work on this Hugo theme itself, you do not need to use git submodules.
Fork and clone this repository like you would a normal git repository.
Then, open a Pull Request when you have changes to propose.


## Main features

The upstream Dot theme includes the following features:

- Automatic search
- Search suggestion
- Syntax highlighting
- Multilingual mode
- Powered by Bootstrap 4
- Google Analytics
- Color schemes
- Next/Prev buttons in single-post page
- Contact Page
- Frequently Asked Questions (F.A.Q.) page
- Responsive-ready


## Share feedback

[Open a new issue on `unicef/inventory` to report bugs and request new features.](https://github.com/unicef/inventory/issues/new/choose)


## Legal

Licensed under [MPL-2.0](https://www.mozilla.org/en-US/MPL/ "About the Mozilla Public License").
From [_choosealicense.com_](https://choosealicense.com/licenses/mpl-2.0/):

> Permissions of this weak copyleft license are conditioned on making available source code of licensed files and modifications of those files under the same license (or in certain cases, one of the GNU licenses).
> Copyright and license notices must be preserved.
> Contributors provide an express grant of patent rights.
> However, a larger work using the licensed work may be distributed under different terms and without source code for files added in the larger work.
