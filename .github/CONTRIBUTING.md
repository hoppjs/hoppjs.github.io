# Contribution Guide

Thanks for thinking of contributing! Before you get started, just make
sure you have a look at this guide so your contribution can be added to
the project efficiently. It's also a guide that we use internally between
the major collaborators of the project!

## Table of Contents

 - [Style Guides](#style-guides)
 - [Pull Requests](#pull-requests)
 - [Naming Branches](#naming-branches)
 - [Modification of Dependencies](#modification-of-dependencies)

## Style Guides

The basic style guide to follow for your HTML &amp; CSS is [codeguide.co](http://codeguide.co/).

Any additional style guides listed in this section should be seen as overriding to this style guide.

### General rules

 - Don't put newlines at the end of files.

### CSS Style Guide

  - First and foremost, our CSS follows the rules of [SUIT CSS](https://github.com/suitcss/suit/blob/master/doc/STYLE.md).
  - We follow a strict property order, the same as Twitter's old internal styleguid - RECESS, which can be found in `stylelint.order.js`. This is so someone reading your CSS can easily find.
  - Rules that start with `@` must always be preceeded with an empty line.
  - Numbers should never have leading zeros. (i.e. it's `.8`, not `0.8`)

### JS Style Guide

 - Linting rules extend [`eslint:recommended`](http://eslint.org/docs/rules/).

## Pull Requests

When adding features or content, please always follow this workflow:

 1. **Ensure that a need for this feature or content is present.** Every feature
 request, bug fix, documentation update, enhancement, etc. should always have its own
 issue associated with it. The issue is the place where discussion happens about whether
 or not that certain problem needs to be addressed and if so, what is the best way to
 do it. Before these discussions take place, no PR should be opened and no code should
 be written in any fork/branch. If no issue exists yet for your idea, create a new issue
 and await proper feedback before implementing it.
 2. **Create a PR as soon as you have code ready.** The existence of the PR shows that work
 is being done on the issue and also provides all contributors and viewers with status updates
 regarding the issue - rather than each contributor having to subscribe to separate branches
 and forks. There are labels to indicate whether the status of a PR - use them to signify
 whether or not your PR needs to be merged yet. Keep these up-to-date as you work.
 3. **Follow the style guides.** For different code changes, there are different style guides
 that we try to stick to. To see a complete list, checkout the section [Style Guides](#style-guides).
 4. **Don't squash your commits.** When you're working on your PR, don't worry about squashing - a
 list of commits is helpful for rollbacks and things like that. But when PRs are merged, we will be
 using Github's "Squash & Merge" feature to ensure that your PR is squashed at the last possible
 moment.
 5. **Internal use: never merge your own PR.** This really only applies to official collaborators of
 the project, but please do not ever merge a PR that you opened. Assign a reviewer and await approval
 for your PR. After approval, still do NOT merge your own PR - let the reviewer do it.

## Naming Branches

For collaborators, this is a set of rules for branch naming that we follow.

For contributors, this is a good way to know what is/isn't being worked on.

 - `master`: active branch that all PRs get merged into - the latest commit will not necessarily be stable. To checkout a stable
 version of master, checkout a tagged commit.
 - `fix_n`: a branch where issue `n` is being fixed.

Code cycle: `fix_n` => `master` => `master#vXX.XX.XX`

## Modification of Dependencies

The dependencies of the project are defined in `bower.json`.

### Modifying Bower Dependencies

  - Updates to the `bower.json` should be absolutely minimal.
  - If it's possible to only commit the single change to the `bower.json` then only commit that.
  - If config files need to be updated/added, add those in your commit.
  - Do NOT modify any other files in a commit that modifies the `bower.json`.