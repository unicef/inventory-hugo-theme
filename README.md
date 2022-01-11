inventory-hugo-theme
====================

<!--
    Style rule: one sentence per line please!
    This makes git diffs easier to read. :)
-->

UNICEF Inventory theme, for use with [Hugo](https://gohugo.io/) static site generator.
Forked from Dot, a Hugo theme by ThemeFisher.


## Examples

* [UNICEF Open Source Inventory](https://unicef.github.io/inventory/)
* [UNICEF Coach Cards](https://unicef.github.io/coach/)
* [UNICEF Drone DPG Toolkit](https://unicef.github.io/drone-dpgtoolkit/)
* [UNICEF Software Development Toolkit](https://unicef.github.io/ooi-toolkit-software/)
* [SustainOSS Design & UX knowledgebase](https://sustainers.github.io/design/)


## Installation

The recommended installation method for an existing Hugo site is with a [git submodule](https://git-scm.com/docs/git-submodule).
Use the commands below to add the theme to an existing Hugo site:

```bash
cd /path/to/hugo-site/
git submodule add git@github.com:unicef/inventory-hugo-theme.git themes/inventory
git commit --signoff --message="Add UNICEF Inventory Hugo theme as a git submodule"
git push
```

### Update a submodule to latest upstream

Sometimes you will want to update the git submodule with new changes added upstream to this repository.
To pull newer upstream changes into your pre-existing git submodule, run the following from your Hugo project root directory:

```bash
git submodule update --remote --rebase
```


## Configuration

See [`sample_config.yaml`](/sample_config.yaml) for a sample Hugo site using this theme.


## Contributing

If you want to work on this Hugo theme itself, you do not need to use git submodules.
Fork and clone this repository like you would a normal git repository.
Then, open a Pull Request when you have changes to propose.


## Features

The upstream Dot theme includes the following features:

- Multiple language support (Fr, En)
- Google analytics support
- CSS and Js bundle with hugo pipe
- Color and fonts variable in config file
- Contact form Support
- Google page speed optimized ( 81% )
- Open graph meta tag
- Twitter card meta tag
- Search suggestions
- Powered by Bootstrap 4
- Next/Prev buttons in single-post page
- Frequently Asked Questions (F.A.Q.) page
- Responsive-ready


## Share feedback

[Open a new issue to report bugs and request new features.](https://github.com/unicef/inventory-hugo-theme/issues/new/choose)


## Legal

Licensed under [MPL-2.0](https://www.mozilla.org/en-US/MPL/ "About the Mozilla Public License").
From [_choosealicense.com_](https://choosealicense.com/licenses/mpl-2.0/):

> Permissions of this weak copyleft license are conditioned on making available source code of licensed files and modifications of those files under the same license (or in certain cases, one of the GNU licenses).
> Copyright and license notices must be preserved.
> Contributors provide an express grant of patent rights.
> However, a larger work using the licensed work may be distributed under different terms and without source code for files added in the larger work.
