# Vscode-CPython-debug

Vscode configuration for debugging CPython.


## Prerequisites:
1. Install [Docker](https://www.docker.com/products/docker-desktop)
2. Install [vscode](https://code.visualstudio.com/download) with [remote-development](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack) plugin


## Setup:
1. Clone [Cpython](https://github.com/python/cpython/tree/v3.8.0).
2. Clone/Download this repo in another location apart from where you cloned Cpython.
3. Copy and Paste the `.devcontainer` and `.vscode` directories into the directory where you cloned CPython.
4. Open Cpython in vscode.
5. Click on the green *Remote action button* " `><` " at the lower leftmost corner in vscode(as shown in the image) and select **Remote-Containers: Open Folder in Container...** from the commands popup that appears, vscode will now start building the container and then build Cpython with relevant flags.

    ![](https://code.visualstudio.com/assets/docs/remote/common/remote-dev-status-bar.png)


## Debug Configurations:
Inside the `.vscode/launch.json` resides the debug configurations, there are three types of debugging configured:

1. `Cpython test`
    
    Debug a CPython test case.
    
    The best way to read the code of any open source project is to debug using the test cases. CPython's test cases are inside `Lib/tests`. Open any of the test case, for eg `Lib/tests/test_list.py`, these are the test cases for good ol python list, each object in Python has its respective implementations inside the directory `Objects` and you can find the list implementation in `Objects/listobject.c`, open the same and set a debug point in `PyList_GetItem` at line 199.
    Now go back to the `test_list.py` and start the debugger, Voila, the debugger breaks exactly at `PyList_GetItem`.

2. `python -c`

    Debug the python process by executing using the `python -c` option.

    Change the statement that you want the Python interpreter to run in the `args` option; currently it is `"args": ["-c", "print(\"hello\")"]`; i.e `python -c "print('hello')"`.

3. `python`

    Launches a Python interpreter and from there you can provide a statement for the interpreter to execute and you can follow along.

## Further reading
Head to [Exploring Cpython](https://devguide.python.org/exploring/), the *Additional References* section has all the exhaustive resources for you to get started with CPython walkthrough! Happy Hacking.
