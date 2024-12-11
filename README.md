# Ansible Workspace for the development of `ansible-collection-redhatci-ocp` code


## About

This repository aims to simplify contributing to [redhatci:ansible-collection-redhatci-ocp|https://github.com/redhatci/ansible-collection-redhatci-ocp]

It is an opinionated, but based on ansible-dev-tools concepts, probably trickling down with "best practices".

## Requirements

1. open unix/linux/mac shell (commands are using `bash`, but converting to other shells is trivial), or equivalent IDE setup
2. to simplify authentications and password prompts, please use `ssh-agent` (the rest of the document assumes ssh transport)
3. you are expected to develop inside your own fork and under non `main` branch.

## Initial Setup

1. Choose workspace root folder conveniently, for example: `${HOME}/src/github.com/$
1. Clone this repository under `workspace` folder, for example as follows:

        gh_user="$(ssh -T git@github.com 2>&1 | cut -d'!' -f1 | cut -d' ' -f2)"
        code_root="${HOME}/src/github.com/${gh_user}"
        mkdir -p "${code_root}" && cd "${code_root}"
        git clone https://github.com/mvk/ansible-collection-redhatci-ocp-workspace workspace

3. edit the submodules file and specify your `ansible-collection-redhatci-ocp` fork url + branch name under
