# Contributing to Scatter

We would love for you to contribute to Scatter and help make it even better than it is
today! As a contributor, here are the guidelines we would like you to follow:

 - [Code of Conduct](#markdown-header-code-of-conduct)
 - [Question or Problem?](#markdown-header-got-a-question-or-problem?)
 - [Issues and Bugs](#markdown-header-found-a-bug?)
 - [Feature Requests](#markdown-header-missing-a-feature?)
 - [Submission Guidelines](#markdown-header-submission-guidelines)
 - [Coding Rules](#markdown-header-coding-rules)

## Code of Conduct
Help us keep Scatter open and inclusive. Please read and follow our [Code of Conduct][coc].

## Got a Question or Problem?

Do not open issues for general support questions as we want to keep GitHub issues for bug reports and feature requests. You've got much better chances of getting your question answered by contacting a developer via email or IM.

## Found a Bug?
If you find a bug in the source code, you can help us by
[submitting an issue](#markdown-header-submitting-an-issue) to our [GitHub Repository][github]. Even better, you can
[submit a Pull Request](#markdown-header-submitting-a-pull-request) with a fix.

## Missing a Feature?
You can *request* a new feature by [submitting an issue](#markdown-header-submitting-an-issue) to our GitHub
Repository. If you would like to *implement* a new feature, please submit an issue with
a proposal for your work first, to be sure that we can use it.
Please consider what kind of change it is:

* For a **Major Feature**, first open an issue and outline your proposal so that it can be
discussed. This will also allow us to better coordinate our efforts, prevent duplication of work,
and help you to craft the change so that it is successfully accepted into the project.
* **Small Features** can be crafted and directly [submitted as a Pull Request](#markdown-header-submitting-a-pull-request).

## Submission Guidelines

### Submitting an Issue

Before you submit an issue, please search the issue tracker, maybe an issue for your problem already exists and the discussion might inform you of workarounds readily available.

We want to fix all the issues as soon as possible, but before fixing a bug we need to reproduce and confirm it. In order to reproduce bugs we will systematically ask you to provide a minimal reproduction scenario using http://plnkr.co. Having a live, reproducible scenario gives us wealth of important information without going back & forth to you with additional questions like:

- version of Scatter used
- 3rd-party libraries / dependencies and their versions
- and most importantly - a use-case that fails

A minimal reproduce scenario using http://plnkr.co/ allows us to quickly confirm a bug (or point out coding problem) as well as confirm that we are fixing the right problem. If plunker is not a suitable way to demonstrate the problem (for example for issues related to our npm packaging), please create a standalone git repository demonstrating the problem.

We will be insisting on a minimal reproduce scenario in order to save maintainers time and ultimately be able to fix more bugs. Interestingly, from our experience users often find coding problems themselves while preparing a minimal plunk. We understand that sometimes it might be hard to extract essentials bits of code from a larger code-base but we really need to isolate the problem before we can fix it.

Unfortunately we are not able to investigate / fix bugs without a minimal reproduction, so if we don't hear back from you we are going to close an issue that don't have enough info to be reproduced.

You can file new issues by filling out our [new issue form][new-issue].


### Submitting a Pull Request
Before you submit your Pull Request (PR) consider the following guidelines:

1. Search [GitHub][pull-requests] for an open or closed PR that relates to your submission. You don't want to duplicate effort.
1. Fork the ```one-two-three-go/scatter``` repo.
1. Make your changes in a new git branch:

     ```shell
     git checkout -b my-fix-branch master
     ```

1. Create your patch, **including appropriate test cases**.
1. Follow our [Coding Rules](#markdown-header-coding-rules).
1. Run the full Scatter test suite, as described in the [developer documentation][dev-doc],
    and ensure that all tests pass.
1. Commit your changes using a descriptive commit message.

     ```shell
     git commit -a
     ```
    Note: the optional commit `-a` command line option will automatically "add" and "rm" edited files.

1. Push your branch to GitHub:

    ```shell
    git push origin my-fix-branch
    ```

1. In GitHub, send a pull request to `scatter:pc_dev`.
* If we suggest changes then:
  * Make the required updates.
  * Re-run the Scatter test suites to ensure tests are still passing.
  * Rebase your branch and force push to your GitHub repository (this will update your Pull Request):

    ```shell
    git rebase master -i
    git push -f
    ```

That's it! Thank you for your contribution!

#### After your pull request is merged

After your pull request is merged, you can safely delete your branch and pull the changes
from the main (upstream) repository:

* Delete the remote branch on GitHub either through the GitHub web UI or your local shell as follows:

    ```shell
    git push origin --delete my-fix-branch
    ```

* Check out the master branch:

    ```shell
    git checkout master -f
    ```

* Delete the local branch:

    ```shell
    git branch -D my-fix-branch
    ```

* Update your master with the latest upstream version:

    ```shell
    git pull --ff upstream master
    ```

## Coding Rules
To ensure consistency throughout the source code, keep these rules in mind as you are working:

* All features or bug fixes **must be tested** by one or more specs (unit tests).


[coc]: ./CODE_OF_CONDUCT.md
[dev-doc]: ./DEVELOPER.md

[github]: https://github.com/one-two-three-go/scatter
[pull-requests]: https://github.com/one-two-three-go/scatter/pull-requests/
[new-issue]: https://github.com/one-two-three-go/scatter/issues/new/

[jsfiddle]: http://jsfiddle.net
[plunker]: http://plnkr.co/edit
[runnable]: http://runnable.com
