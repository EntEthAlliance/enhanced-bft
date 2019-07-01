# Contributing to the EEA Client Specification

This specification is developed on an ongoing basis. Releases are made periodically by the EEA Technical Specification Working Group (TSWG).

Contributions are governed by the EEA governance documents, and the [EEA License](LICENSE.md)

## Table of Contents

* [How to raise an issue or question](#issues)
* [How to propose a change (Pull Requests)](#PRs)
* [How Issues and Pull Requests are Processed](#how)
* [More Questions?](#faq)

<h2 id="issues">To ask a question, raise an issue, or suggest a change is needed:</h2>

1. Check for an an [existing GitHub issue](https://github.com/EntEthAlliance/client-spec/issues) on the same topic.
1. If there is not an existing GitHub issue, [create one](https://github.com/EntEthAlliance/client-spec/issues/new) explaining the problem the change is meant to resolve.

The [EEA Slack Channel](https://entethalliance.slack.com) is a useful place to ask a quick question,
but for comments on an issue to be considered they should be archived in the issue itself.

<h2 id="PRs">To propose a specification change (to address an issue):</h2>

<img style="float:right;width:350px" alt="On the right hand side of the issue page are links to assign issues and set labels and milestones" src="images/workflow/assign-etc.png">

1. Assign the GitHub issue to yourself.
1. Select a **milestone**. This means that you expect to have a Pull Request by the closing date of the milestone.
1. Create a Pull Request. Please note the [source code conventions](source-guide.md) to ensure your Pull Request is in an appropriate format.

   [github_workflow.md](github_workflow.md) describes a simple way to do this through the GitHub Website.

   You can also [clone](https://help.github.com/articles/cloning-a-repository/) the repository to your computer,
   create a branch, make your edits, and create a Pull Request against the Master branch, using the GitHub Desktop client, or Git's Command Line Interface.

<h2 id="TF-SIG">For other Working Groups, Task Forces and SIGs, ...</h2>

* To note that a GitHub issue is relevant to a particular group, select the **label** of that group's name.
* To indicate that a Pull Request is supported by a particular group, please select the **label** of that group's name.
* Group Chairs should review all issues and Pull Requests with their group's label at least as often as the group meets

<h2 id="how">How Issues and Pull Requests are processed</h2>

Resolution of an issue can be proposed for any milestone. Proposed resolutions are added to the associated meeting agenda.
If there is no objection before the meeting and consensus in the meeting, the resolution will be adopted.
If there are requests for non-editorial changes to the resolution, it will be held open to build consensus on a proposal.

Issues will be closed when a Pull Request addressing the issue is merged,
or a decision is reached that the issue will not be resolved.

Depending on the clarity of the proposed resolution, issues will be categorised using one of the two following labels in GitHub, in preparation for the milestone they are associated with:
- *Bulk resolution* for those issues that can be closed as proposed without individual resolution or discussion
- *Individual resolution* for those issues requiring individual resolution or discussion

An issue deferred for further consideration will not normally be closed.
If the chairs and editors do not believe we can resolve it in time for incorporation int he upcoming release,
it may be assigned to the "When it's ready" milestone.

Branches should be deleted after they are merged (or the Pull Request is closed unmerged).
New Pull Requests should be made on a new branch.

<h2 id="faq">More questions?</h2>

If you have questions or doubts about how to proceed, contact Chaals Nevile - @chaals chaals@entethalliance.org, or
Conor Svensson - @conor10 conor@web3labs.com
who can help to ensure your proposal is correctly framed and considered in a timely manner.
