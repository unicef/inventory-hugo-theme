Contributing to UNICEF Inventory theme
======================================

<!--
    Style rule: One sentence per line please!
    This makes git diffs easier to read in Pull/Merge Requests.
-->

Thanks for your interest in contributing to the UNICEF Inventory theme!
The UNICEF Inventory theme is a [Hugo](https://gohugo.io) theme to create a lightweight knowledgebase site.
This page is a guide for making successful contributions to the project.

**Table of contents**:

1. [Contribution process](#process)
1. [Conventions & courtesies](#conventions)
    1. [Start working on an issue](#conventions--issue-start)
    1. [Inactive issues](#conventions--issue-inactive)
    1. [Submit a pull request](#conventions--submit-pr)
    1. [Maintainer response time](#conventions--maintainer-response)
1. [Structure & components](#components)
    1. [Theme](#components-theme)
    1. [Example site](#components-example)
1. [How to create a development environment](#dev-env)
    1. [Requirements](#dev-env--requirements)
    1. [Set up the environment](#dev-env--setup)
    1. [Run the Hugo server](#dev-env--run-hugo)


## <a id="process"></a>Contribution process

The UNICEF Inventory theme is managed as a tool of the [UNICEF Venture Fund](https://www.unicefinnovationfund.org/) within the [UNICEF Office of Innovation](https://www.unicef.org/innovation/).
New contributions to the UNICEF Inventory theme are reviewed and managed by the UNICEF Ventures folks responsible for working with our team's open source technology.
Decisions about the project are generally headed up by a specific tech lead assigned to the project.
**As of 2022, this is currently [Justin W. Flory](https://github.com/jwflory).**

Since the team is small and our efforts are still early, this project's governance is fluid and may change over time to help us grow and scale, as needed.


## <a id="conventions"></a>Conventions & courtesies

This section describes conventions and common courtesies when working on the project.
Following these steps improves the probability of your change or contribution being accepted.

### <a id="conventions--issue-start"></a>Start working on an issue

Want to work on a new issue?
Follow these steps:

1. Check if issue is already assigned
1. Leave a comment in the issue to work on it
1. Start a new git feature branch

If someone else is already assigned, it means the task is **already in progress**.
An assigned issue is not available to start new work.
If an issue has no updates for longer than seven days, you may follow up and ask if the assignee is still working on the issue.

Then, **leave a comment** in the issue you want to work on.
A maintainer will reply asking for more information or they will assign the issue to you.
When you are assigned an issue, this means you are approved to work on it.

Finally, once approved to work on an issue, **create a new [git feature branch](https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow)** for the issue you are working on.
This will help you [make a pull request](#conventions--submit-pr) and make revisions easier.

### <a id="conventions--issue-inactive"></a>Inactive issues

Sometimes, an assignee of an issue may no longer have time to work on an issue.
**After five days of no updates, an issue can be reassigned by a project maintainer.**
This _DOES NOT_ mean all issues must be solved in five days.
It _DOES_ mean if an assignee does not respond to new comments in an issue after five days of their last comment, it can be re-assigned by a maintainer.
This helps to keep issues open and available for those who have time to work on them.

If you are working on an issue and more than five days have passed since your last comment, please give an update when possible.

### <a id="conventions--submit-pr"></a>Submit a pull request

These guidelines help maintainers review new pull requests.
Stick to the guidelines for faster pull request reviews.

1. Prefer gradual small changes than sudden big changes.
1. Write meaningful commit messages.
   Commit messages should be clear and brief.
   Tag an issue in your commit message if you are assigned an issue, e.g. `Fixes #123.`
1. Write a helpful title for your pull request (if someone reads only one sentence, will they understand your change?)
1. Address the following questions in your pull request:
    1. What is a summary of your change?
    1. Why is this change helpful?
    1. Any specific details to consider?
    1. What do you think is the outcome of this change?
1. Include screenshots of before/after if your change is a front-end change.

### <a id="conventions--maintainer-response"></a>Maintainer response time

Project maintainers / mentors are committed to **no more than three days for a reply** during Outreachy rounds.
If more than three days have passed and you have not received a reply, follow up in [our Matrix room](https://matrix.to/#/#unicef-innovation:matrix.org).
Someone may have missed your comment.

_Remember_, using issue templates and answering the above questions in pull requests reduces response time from a maintainer to your issue / Pull Request.


## <a id="components"></a>Structure & components

The UNICEF Inventory theme includes two components: the theme and an example site (used as a proof-of-concept to demonstrate capabilities of the theme).

### <a id="components-theme"></a>Theme

The website theme that provides the interface and UX of the public website is the [UNICEF Inventory theme](https://github.com/unicef/inventory-hugo-theme).
It is a theme made for the [Hugo static site generator](https://gohugo.io/).
For changes to the site look-and-feel, user interface, and user experience, you can open bug reports, feature requests, and ideas in the [issue tracker](https://github.com/unicef/inventory-hugo-theme/issues) of the UNICEF Inventory theme.

The content you find published in the [public website](https://sustainers.github.io/design) is hosted here.
You can find all the content in the [`content/` directory](/content/) of this repository.
For changes to content, categories, and the text published on the website, this repository is the place to have discussions, submit changes, and collaborate with the Design & UX Working Group.

### <a id="components-example"></a>Example site

There is also an example site included in the theme.
It demonstrates basic features and look-and-feel of the theme.
You can find the example site in the [`exampleSite/` directory](/exampleSite/) of this repository.
This example site also acts as the documentation for the Hugo theme as well.


## <a id="dev-env"></a>How to create a development environment

So, you want to work on the UNICEF Inventory theme?
Great!
This section describes how to set up a development environment using Hugo.
A development environment is needed to test changes and build the site locally.
While it is helpful for reviewing changes, it is not required so long as the continuous integration pipeline is passing on a Pull Request.

### <a id="dev-env--requirements"></a>Requirements

To create a developer environment, you must install the following:

* [Hugo](https://gohugo.io/getting-started/installing/)
* [git](https://github.com/git-guides/install-git) or a git client

### <a id="dev-env--setup"></a>Set up the environment

First, create a fork of the repository to your GitHub account.
Clone the git repository for **your fork** of the UNICEF Inventory theme:

```sh
git clone git@github.com:your-username-here/inventory-hugo-theme.git
```

### <a id="dev-env--run-hugo"></a>Run the Hugo server

Finally, you will use Hugo to run a local HTTP web server and generate a preview of the site from your own machine.
You must start the Hugo server from the directory containing the example site.
Simply change directories to the example site, and run the Hugo server:

```sh
cd /path/to/repo/
cd exampleSite/
hugo serve
```

The terminal will print a message with a URL to the local preview, such as [localhost:1313/inventory-hugo-theme/](http://localhost:1313/inventory-hugo-theme/).
Direct your browser to the local preview, and it should appear just as it does on the public website.
