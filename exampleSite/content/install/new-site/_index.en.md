---
title: Create a new Hugo site
description: Learn how to create a new Hugo site using the UNICEF Inventory theme.
tags: ["forking", "git", "new site"]
downloadBtn: true
# search keywords
keywords: ["fork", "forking", "install", "installation", "launch"]

---

This page documents how to create a new Hugo website using the UNICEF Inventory theme.
You need to already understand the basics of Hugo.
If you do not know about Hugo, review the [Hugo documentation on getting started](https://gohugo.io/getting-started/) to learn more about the basics.

## Overview

This guide assumes you will use GitHub to host the source content for your website and GitHub Pages to deploy the generated HTML built by Hugo.
To create a new Hugo website with the UNICEF Inventory theme, you will need to complete the following steps:

1. [Create a git repository for your project](#create-git)
1. [Add the UNICEF Inventory theme as a git submodule](#install-theme)
1. [Configure your Hugo website](#configure-hugo)
1. [Create content in your website](#create-content)
1. [Preview the website locally](#preview-locally)
1. [Deploy to GitHub Pages](#deploy-github)


## Create a git repository for your project {#create-git}

First, you need to create a new Hugo site on your workstation, initialize a local git repository, and push your local changes to a remote git repository.

To begin, you need to create a new Hugo site with the source content.
**Source content** refers to the content files, Hugo configuration file, and other text files used to build the final HTML website.
Hugo provides a handy command to bootstrap a new website and generate initial source content (`hugo new site <website_name>`).
However, this command also creates several sub-directories and files you will not need for the UNICEF Inventory theme.
Alternatively, create the following sub-directories within the website directory for your new Hugo website:

```bash
mkdir content/ static/ themes/
```

Next, you need to initialize a local git repository in your Hugo website directory.
Note, if you already have an existing remote git repository, you should skip this step and instead clone the remote repository locally to your workstation.
To initialize a new git repository with the UNICEF Inventory theme configuration, use the following commands:

```bash
# Initialize a new git repository.
git init

# Copy the config file from this website to use as a base for your own site. If `curl`
# is not installed in your $PATH, you can also manually copy the file from GitHub and
# add it to your Hugo website directory.
curl --location --output config.yaml https://raw.githubusercontent.com/unicef/inventory-hugo-theme/main/exampleSite/config.yaml

# Create the first commit in your git repository.
git add .
git commit --signoff --message="Initial commit"
```

Finally, you need to push your local changes to a remote git repository hosted on a site like GitHub.
This example guide uses GitHub for the remote git repository, but you can use any git hosting platform like GitLab, Pagure, or any other.
Note that the git hosting platform you choose may have implications on the hosting (see [Deploy to GitHub Pages](#deploy-github) for more information).
Your git hosting platform should give you instructions on how to push local changes if it is unclear.
The commands needed should look like this:

```bash
git remote add origin git@github.com:myname/myrepo.git
git push --set-upstream origin main
```

Now, your local git repository is synchronized with the remote git repository.


## Add the UNICEF Inventory theme as a git submodule {#install-theme}

The recommended way to install the UNICEF Inventory theme into your Hugo website is to add it as a **git submodule**.
Using a git submodule provides an easier method to get changes, improvements, and bug fixes from the upstream theme in your downstream Hugo site.

While you are in your Hugo website directory, use the following commands to initialize a git submodule with the UNICEF Inventory theme:

```bash
git submodule add --name inventory https://github.com/unicef/inventory-hugo-theme.git themes/inventory
```

This initializes a new git submodule with the UNICEF Inventory theme.
It also creates a `.gitmodules` file in addition to cloning the theme repository inside of your Hugo website repository.
Make sure to commit these files into your git repository.

{{% notice tip %}}
Did you clone a repository with a `.gitmodules` file, but missing the repository in `themes/inventory`?
Use this command to clone the submodule when it is already defined in the `.gitmodules` file:

```bash
git submodule update --init
```
{{% /notice %}}

Alternatively, you can download the UNICEF Inventory theme [as a `.zip` file](https://github.com/unicef/inventory-hugo-theme/archive/refs/heads/main.zip) file and extract it in the `themes` directory.
However, this is not recommended as you will be responsible for manually updating changes, improvements, and bug fixes introduced in the upstream UNICEF Inventory theme.


## Configure your Hugo website {#configure-hugo}

The easiest way to configure your Hugo website is to copy the [example site `config.yaml`](https://raw.githubusercontent.com/unicef/inventory-hugo-theme/main/exampleSite/config.yaml) and modify it to fit your needs.
See the [Features category]({{< ref "/features" >}}) for more guidance on configuring different components of the UNICEF Inventory theme.


## Create content in your website {#create-content}

Next, you need to create source content in your Hugo website.
The UNICEF Inventory theme supports **Markdown** and **AsciiDoc** as source content markup languages.
Create a new page either by manually creating files in `content/` or using this shortcut command:

```bash
hugo new my-category/_index.en.md
hugo new my-category/hello-world.en.md
```

Edit these files by adding front-matter and content into the files.
The front-matter for this page is shown below as an example:

```yaml
---
title: Create a new Hugo site
description: Learn how to create a new Hugo site using the UNICEF Inventory theme.
tags: ["forking", "git", "new site"]
downloadBtn: true
# search keywords
keywords: ["fork", "forking", "install", "installation", "launch"]

---
```


## Preview the website locally {#preview-locally}

Now, you can preview your Hugo website locally from your own workstation before pushing your changes to the remote git repository.
Build the Hugo website and preview the changes with the following command:

```bash
hugo serve
```

Click the URL from the console output to view a local preview of the website.


## Deploy to GitHub Pages {#deploy-github}

See Hugo documentation on [deploying your Hugo website to GitHub Pages](https://gohugo.io/hosting-and-deployment/hosting-on-github/).
You will need a continuous integration (C.I.) pipeline to help you deploy changes to a hosting service provided by your git hosting platform.

The UNICEF Open Source Inventory uses [Circle CI](https://circleci.com/) to build its changes, validate the HTML, and deploy to GitHub Pages.
Find the Circle CI configuration file and deployment script [here](https://github.com/unicef/inventory/tree/main/.circleci).
