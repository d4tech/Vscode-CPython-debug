# Vscode-CPython-debug

Vscode configuration for debugging CPython.


## Prerequisites:
1. Install [Docker](https://www.docker.com/products/docker-desktop)
2. Install [vscode](https://code.visualstudio.com/download) with [remote-development](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack) plugin


## Setup:
1. Clone [Cpython3.6](https://github.com/python/cpython/tree/v3.6.8) or clone the CPython master branch and do a `$git checkout v3.6.8`.
2. Clone/Download this repo in another location apart from where you cloned Cpython.
3. Copy and Paste the `.devcontainer` and `.vscode` directories into the directory where you cloned CPython.
4. Open Cpython in vscode.
5. Click on the green *Remote action button* " `><` " at the lower leftmost corner in vscode(as shown in the image) and select **Remote-Containers: Open Folder in Container...** from the commands popup that appears, vscode will now start building the container and then build Cpython with relevant flags.

    ![](https://code.visualstudio.com/assets/docs/remote/common/remote-dev-status-bar.png)

## Known Issues:
* Cannot work with Python3.8 because of linker issues, within Docker.