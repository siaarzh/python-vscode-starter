# Python + VS Code + Remote Development

A quick start guide. ([DEV post](https://dev.to/siaarzh/vs-code-with-python-in-docker-quickstart-3ph4))

## Instructions

1. Install [VS Code Insiders](https://code.visualstudio.com/insiders/) edition and the [Remote Development](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack) extension pack
2. Start a new project by opening a new directory with VS Code Insiders and create a *requirements.txt* file with the Python packages you wish to have, e.g.:

        django==2.2.2

3. <kbd>ctrl</kbd>+<kbd>shift</kbd>+<kbd>p</kbd> and start typing "remdev", select "Remote-Containers: Add Dev Container Configuration Files..."
4. Search for "pypo" and select "Python 3 & PostgreSQL" as your environmet. This
will create a _.devcontainer_ folder with the files:
    - devcontainer.json
    - docker-compose.yml
    - Dockerfile
    - noop.txt

5. <kbd>ctrl</kbd>+<kbd>shift</kbd>+<kbd>p</kbd> and start typing "rerefo", select "Remote-Containers: Reopen Folder in Container"
6. Start coding ☕💻

### A Note on Forwarding Ports

So how do you open a port to your container? Easy! VS Code already knows which ports are open in your container.

Say you started your server with `python manage.py runserver`, which would open a port on 127.0.0.1:8000 in your container. VS Code is aware of this and will give you the option to forward your system ports to that port.

Press <kbd>ctrl</kbd>+<kbd>shift</kbd>+<kbd>p</kbd>, search "port" and select "Remote-Containers: Forward Port from Container...". A list of open ports will come up, select port 8000.

## References

- [Container Remote Development](https://code.visualstudio.com/docs/remote/containers) with VS Code
- [Django Tutorial part 1](https://docs.djangoproject.com/en/2.2/intro/tutorial01/)

## TODO

- add requirements (base + dev) files