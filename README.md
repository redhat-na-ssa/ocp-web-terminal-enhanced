# OpenShift Enhanced Web Terminal

[![Spelling](https://github.com/redhat-na-ssa/ocp-web-terminal-enhanced/actions/workflows/spellcheck.yaml/badge.svg)](https://github.com/redhat-na-ssa/ocp-web-terminal-enhanced/actions/workflows/spellcheck.yaml)
[![Linting](https://github.com/redhat-na-ssa/ocp-web-terminal-enhanced/actions/workflows/linting.yaml/badge.svg)](https://github.com/redhat-na-ssa/ocp-web-terminal-enhanced/actions/workflows/linting.yaml)

[![Build](https://github.com/redhat-na-ssa/ocp-web-terminal-enhanced/actions/workflows/build-web-terminal.yaml/badge.svg)](https://github.com/redhat-na-ssa/ocp-web-terminal-enhanced/actions/workflows/build-web-terminal.yaml)

The [OpenShift Web Terminal](https://docs.openshift.com/container-platform/4.14/web_console/web_terminal/installing-web-terminal.html) offers an extensible solution to those who want to run CLI tools in a browser based terminal.

This repo is intended to provide additional tools and a pattern to customize the web terminal.

## Quick Start

Use an [OpenShift Web Terminal](https://docs.openshift.com/container-platform/4.14/web_console/web_terminal/installing-web-terminal.html)

```sh
# git clone
https://github.com/redhat-na-ssa/ocp-web-terminal-enhanced.git
cd ocp-web-terminal-enhanced

# make enhanced web terminal persistent
until oc apply -k bootstrap/web-terminal; do : ; done

# delete old workspaces
oc -n openshift-terminal delete devworkspace --all
```

## Build

```sh
cd container
./download_tools.sh

podman build -t web-terminal-tooling:local .
podman run -it --rm -v $(pwd):/data:z web-terminal-tooling:local /bin/bash
```

## Contributions

Please run the following before submitting a PR / commit

```sh
./lint.sh
```

## Links

- [Docs - Install OpenShift Web Terminal](https://docs.openshift.com/container-platform/4.12/web_console/web_terminal/installing-web-terminal.html)
- [GIT - Web Terminal Operator](https://github.com/redhat-developer/web-terminal-operator)
- [GIT - Web Terminal Tooling Container](https://github.com/redhat-developer/web-terminal-tooling)
- [GIT - GitOps Catalog](https://github.com/redhat-na-ssa/demo-ai-gitops-catalog)
