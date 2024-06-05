# OpenShift Enhanced Web Terminal

The OpenShift Web Terminal offers an extensible solution to those who want to run CLI tools in a browswer based terminal.

NOTE: In process of moving this work from another repo [here](https://github.com/redhat-na-ssa/demo-ai-gitops-catalog) `components/containers/web-terminal`

This repo is intended to provide additional tools and a pattern to customize the web terminal.

## Build

```sh
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
- https://github.com/redhat-na-ssa/demo-ai-gitops-catalog
