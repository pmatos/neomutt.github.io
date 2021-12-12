---
title:       Build and Test
description: Build the code and run some tests
source:      https://github.com/neomutt/neomutt/blob/master/.github/workflows/build-and-test.yml
badge:       https://github.com/neomutt/neomutt/actions/workflows/build-and-test.yml/badge.svg?branch=master&event=push
logs:        https://github.com/neomutt/neomutt/actions/workflows/build-and-test.yml
author:      flatcap
---

<div style="float: right;">
<a href="https://github.com/neomutt/neomutt/actions/workflows/build-and-test.yml"><img src="https://github.com/neomutt/neomutt/actions/workflows/build-and-test.yml/badge.svg?branch=master&event=push" /></a>
<a href="https://lgtm.com/projects/g/neomutt/neomutt"><img src="https://img.shields.io/lgtm/alerts/github/neomutt/neomutt" /></a>
</div>

# {{ page.title }}

{:.subtitle}
{{ page.description }}
{% include actions-links.html %}

## Description

This action is the workhorse of NeoMutt.  It's run on all code that's pushed to
the neomutt repo and all pull requests.

The action performs three builds, with a variety of `configure` options, and a
set of unit tests on some of the libraries.

**Steps**:
- Build Neomutt
- Build Tests
- Run Tests

### Action Details

| Key     | Description                                                    | Details                                                                                        |
| :------ | :------------------------------------------------------------- | :--------------------------------------------------------------------------------------------- |
| Trigger | `git push`                                                     | To branches `master` or `devel/*`                                                              |
| Trigger | Pull Request                                                   |                                                                                                |
| Uses    | GitHub's checkout action                                       | [https://github.com/actions/checkout](https://github.com/actions/checkout)                     |
| Uses    | [Hendrik Muhs](https://github.com/hendrikmuhs)' ccache-action  | [https://github.com/hendrikmuhs/ccache-action](https://github.com/hendrikmuhs/ccache-action)   |
| Runs-on | ubuntu-latest                                                  | [neomutt/docker-build](https://ghcr.io/neomutt/docker-build)                                   |

### See Also

| Description | Location                                                                                       |
| :---------- | :--------------------------------------------------------------------------------------------- |
| Action      | [{{page.source}}]({{page.source}})                                                             |
| Action Logs | [{{page.logs}}]({{page.logs}})                                                                 |
| Source Code | [https://github.com/neomutt/neomutt](https://github.com/neomutt/neomutt)                       |
| Test Files  | [https://github.com/neomutt/neomutt-test-files](https://github.com/neomutt/neomutt-test-files) |
