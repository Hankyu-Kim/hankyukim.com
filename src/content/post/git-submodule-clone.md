---
title: "git submodule clone"
publishDate: "09 Jun 2024"
description: "--------------------------------------------------"
tags: ["Git"]
draft: true
---

Let's clone the project with submodules!

```bash
git clone {git address}
```

When you clone a project with submodules, you might find the submodule directories are empty. This happens because, by default, Git does not automatically clone the content of submodules. If a project has hundreds of submodules, it can be inefficient to retrieve all the submodule content when you only need to fix a few lines in the main project. Additional steps are required to clone the project with its submodules.

First, use the `git submodule init` command to set up the local configuration file based on the project's submodule settings. Then, the `git submodule update` command retrieves the submodule data from the remote repository, including the commit information for the current project, and checks out the submodule.

```bash
git submodule init
git submodule update
```

You can follow these steps manually, or you can simplify the process by using the `--recurse-submodules` option when cloning the project. This option automatically initializes and updates all submodules.

```bash
git clone --recurse-submodules {git address}
```