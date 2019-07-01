# Github Workflow for the Enterprise Ethereum Alliance Client Specification

This document describes how to contribute to the Enterprise Ethereum Alliance (EEA) Client Specification for those who are new to, or still learning about, using Github.

## Table of Contents

- [Getting Set Up](#getting-set-up)
- [Using the Github Website interface](#using-the-github-website-interface)
  - [1. Edit the Document](#1-edit-the-document)
  - [2. Create a Pull Request](#2-create-a-pull-request)
- [Using the Desktop Client](#using-the-desktop-client)
  - [1. Clone the Repository](#1-clone-the-repository)
  - [2. Create a Branch](#2-create-a-branch)
  - [3. Make and Commit Changes](#3-make-and-commit-changes)
  - [4. Preview your changes](#4-preview-your-changes)
  - [5. Create a Pull Request](#5-create-a-pull-request)
- [Merging Pull Requests](#merging-pull-requests)
- [Terms](#terms)


## Getting Set Up

To make contributions to the Specification, you require a [Github](#github) account authorized to access the Specification [repository](#repository). Viewing this page requires such an account, so your Github account is already authorized.

You may want to use the [Github Desktop](#github_desktop) client on your Mac or Windows system. Otherwise you can use Github's Web interface to make all changes.

## Using the Github Website interface

The Github website offers a simple mechanism to make changes to documents.

### 1. Edit the document

1. Select the document in the repository you want to edit, for example [the Specification source: **spec.html** in the **docs** folder](docs/spec.html)
1. Click the edit button ![editbutton.png](images/workflow/editbutton.png) in the top right corner.
1. Edit the text to make your proposed changes

At any time while editing, you can preview your changes by switching to the "Preview" button. The content will be presented with markers for new text, deleted text, and changed text: ![preview-example.png](images/workflow/preview-example.png)

### 2. Make a Pull Request for your changes

1. Below the editing area, provide a descriptive title for your change. If the change is purely editorial, prefix the title with "Editorial":
   > Editorial: clarify the documentation
1. Describe what has changed.
1. Select "create a new branch" ![new-branch.png](images/workflow/new-branch.png) and give it a name. A useful convention is to provide your Github ID, and one or two keywords, and related issue numbers (if any), e.g.
   > chaals-add-sync-get-method-55
1. Click the "Commit changes" button: !["Commit changes" button](images/workflow/commit_changes.png)

Github will create a new [branch](#branch), and offer to create a Pull Request   

1. If you want someone else to review your proposal, type their Github username into the reviewer field ![reviewer field](images/workflow/reviewer.png) and select the person you want to do the review.
1. Check that the descriptions are helpful.
1. If the change fixes one or more issues, identify them explicitly by number in the extended description, with a line on its own such as
   > Fix #49, #51
1. Click the "create pull request" button !["create pull request" button](images/workflow/createPR.png)

Github will automatically create a Pull Request, a link to it from any issues you have mentioned, and notify those subscribed to the repository that a new Pull Request has been created.

## Using the Desktop Client

Using the Github Desktop client you can work with a local copy of the repository on your computer.
This allows you to work with any text-editing software, and work offline.

Let's look at the steps involved to make a change:

### 1. Clone the Repository

Making a local clone of the remote Specification [repository](#repository) is usually a one-time operation. After making a clone, most operations are performed on your local [repository](#repository).

To clone the Specification repository:

1. Sign in to [Github](#github) and [Github Desktop](#github_desktop).
2. On the Specification's repository page ([https://github.com/EntEthAlliance/client-spec](https://github.com/EntEthAlliance/client-spec)), click **Clone or download**.

   ![Clone or download](images/workflow/clone_or_download.png)

3. Click **Open in Desktop** to [clone](#clone) the [repository](#repository) and open it in [Github Desktop](#github_desktop).

   ![Open in Desktop](images/workflow/open_in_desktop.png)

4. Click **Choose...**, then navigate to a local path where you want your [cloned](#clone) [repository](#repository) to reside.

   ![Clone a repository](images/workflow/clone_a_repository.png)

5. Click **Clone**.

### 2. Create a Branch

To produce an edited version of the specification to propose a change, you will need to create a [branch](#branch), or presonal copy, of the `master` branch.

In your [branch](#branch) you can edit the content without affecting other branches. This means you can experiment with different ideas before having the changes reviewed and potentially merged into the  `master` branch.

To create a [branch](#branch):

1. Select the "branch" menu, and in the dropdown press the "new branch" button.
   <img src="images/workflow/desktop-newbranch.png" alt="">      
   * Normally, your branch should be created from the `master` branch, but you can also create it based on an existing branch,
     for example to propose an edit to an existing change proposal.
2. Provide a name for your [branch](#branch).
   As a convention, name your [branches](#branch) with your [Github](#github) user name, followed by the purpose of the [branch](#branch), and any issue number it addresses. For example, `username-must-encrypt-pii-240` or `username-section6.1-edits`.
3. Click the blue **Create branch:** button, or just press "Enter".

The message "Branch created." should display at the top of the screen and the drop-down at the top of the file list should now read **branch: \<new branch name\>**.

This indicates you are now working on your new [branch](#branch). Any edits you make are being made to the files in your new [branch](#branch), not `master`.

### 3. Make and Commit Changes

To make and [commit](#commit) changes to a file:

1. Check that you are working in the correct [branch](#branch) (that is, **not** `master`), **before** you open a file for editing.
   If necessary close the file without saving, and re-open it when you have switched to the right branch.
2. Open the file in your preferred editor, and make the changes you want, and save the file.
3. To commit the changes to your current branch, use the changes tab in the Desktop Client. Provide a summary and description for your changes, and press the "commit to ..." button to [commit](#commit).

   You can commit changes progressively to a branch, e.g. by selecting a particular set of files for each commit,
   or by making progressive sets of edits, and saving and committing them.
   This enables review of logical steps rather than only as a single wholesale change.

Your [branch](#branch) now has content that is different from `master`.

### 4. Preview your changes

You can preview your changes as they will be rendered by opening [docs/spec.html](docs/spec.html) in a browser. **Note** This will not work if you are offline. It may not work if you have introduced certain errors to the source code, such as [incorrect reference syntax](source-guide.md).

### 5. Create a Pull Request

A [pull request](#pull_request) is a _request_ for someone to merge your changes into another branch (typically the `master` branch which is the editors' draft of the specification).

To create a [pull request](#pull_request):

1. In the "Branch" menu of the Desktop Client, select "create pull request".
   You may see a dialog saying you need to publish your branch before making the pull request. Select "Publish Branch"
1. The GitHub website will open with a page that allows you to create a Pull Request.
   1. Provide a short description of the change for a title
   2. If the change is a fix for a specific issue include the following text on a separate line of the description:

      ```
      Fix #49
      ```
      If the change is related to one or more issues, but does not change them, include the following text instead:

      ```
      See also #49, #50
      ```
      Including `#<issue number>` in the description automatically creates a link to the issue in the [pull request](#pull_request).
   3. Click **Create pull request**.
1. If you want a specific person to review the Pull Request, select them from the **reviewers** link. Note that some reviewers might already be suggested, but if you leave this blank the editorial team will assign review amongst themselves.
1. Optionally, select appropriate labels

**Note** After you have created a Pull Request, you can continue to edit the branch. If you would like to do so, please add the label "Not Ready for Merging" while you continue to make changes, and remove it when you are ready.

## Merging Pull Requests

**Note:** [Pull requests](#pull_request) are merged by administrators or editors of the [repository](#respository) only. This step is informational.

To merge the [pull request](#pull_request):

1. An Editor or chair reviews the changes in the [pull request](#pull_request).
2. If acceptable, potentially with editorial changes e.g. to fix source code errors, they merge the Pull Request and delete the branch.
3. Otherwise, they comment on what needs to change. The [pull request](#pull_request) is sent back to you for further work.

## Terms

The following table lists and describes some important terms when working with Git and Github.

Term | Description
---- | -----------
<a name="repository">Repository</a> | A container used to organize all the files for a project.<br><br>Repositories can contain folders and files, images, videos, spreadsheets, and data sets – anything your project needs. Often referred to as a _repo_.<br><br>The repository for the Specification is at [https://github.com/EntEthAlliance/client-spec](https://github.com/EntEthAlliance/client-spec).
<a name="clone">Clone</a> | A local copy of a remote [repository](#repository).
<a name="branch">Branch</a> | A copy, or a snapshot, of a [repository](#repository) at a given point in time.<br><br>Using [branches](#branch) is how multiple contributors can work on different versions of a [repository](#repository) at the same time. [Repositories](#repository) have one default [branch](#branch) called `master`. As the name suggests, this is the definitive [branch](#branch) for the [repository](#repository).
<a name="commit">Commit</a> | Save changes to a [branch](#branch).
<a name="pull_request">Pull Request</a> | A _request_ for someone to review your changes and then _pull_ and [merge](#merge) your changes into their [branch](#branch). Often abbreviated as _PR_.
<a name="merge">Merge</a> | Apply changes from one [#branch](branch) in another - e.g. into the master branch.<br><br>For contributions to the Specification, a reviewer (usually an administrator or editor) reviews the changes in a [pull request](#pull_request), and if the changes are acceptable, they are merged with `master`.
<a name="github_desktop">Github Desktop</a> | An application to perform [Github](#github) operations. Alternatives are to do this through the GitHub.com website using a browser, or as a set of command line functions in a terminal.
