# OpenShift Enhanced Web Terminal

[![Spelling](https://github.com/redhat-na-ssa/ocp-web-terminal-enhanced/actions/workflows/spellcheck.yaml/badge.svg)](https://github.com/redhat-na-ssa/ocp-web-terminal-enhanced/actions/workflows/spellcheck.yaml)
[![Linting](https://github.com/redhat-na-ssa/ocp-web-terminal-enhanced/actions/workflows/linting.yaml/badge.svg)](https://github.com/redhat-na-ssa/ocp-web-terminal-enhanced/actions/workflows/linting.yaml)
[![Build](https://github.com/redhat-na-ssa/ocp-web-terminal-enhanced/actions/workflows/build-web-terminal.yaml/badge.svg)](https://github.com/redhat-na-ssa/ocp-web-terminal-enhanced/actions/workflows/build-web-terminal.yaml)

The OpenShift Web Terminal offers an extensible solution to those who want to run CLI tools in a browser based terminal.

NOTE: In process of moving this work from another repo [here](https://github.com/redhat-na-ssa/demo-ai-gitops-catalog) `components/containers/web-terminal`

This repo is intended to provide additional tools and a pattern to customize the web terminal.

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
lint.sh
```

## Links

- https://github.com/redhat-developer/web-terminal-operator
- https://github.com/redhat-developer/web-terminal-tooling
- https://github.com/redhat-na-ssa/ocp-web-terminal-enhanced
