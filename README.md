# Vscode-CPython-debug

Vscode configuration for debugging CPython.


## Prerequisites:
1. [Docker](https://www.docker.com/products/docker-desktop)
2. [vscode](https://code.visualstudio.com/download) with [remote-development](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack) plugin


## Setup:
1. Clone [Cpython3.6](https://github.com/python/cpython/tree/v3.6.8).
2. Clone/Download this repo in another location apart from where you cloned Cpython.
3. Copy and Paste the `.devcontainer` directory into your Cpython directory.
4. Open Cpython in vscode.
5.  Select **Remote-Containers: Open Folder in Container...** from the command list that appears, and open the root folder of the project you just cloned.

    ![](https://code.visualstudio.com/assets/docs/remote/common/remote-dev-status-bar.png)

## Known Issues:
* Cannot work with Python3.8 because of linker issues.