# Arduino IDE 2.x Docker Template

This repository provides a Dockerized template for develop your projects using Arduino IDE 2.x.

## Getting Started

### Prerequisites

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

### Build and Run

1. Create your repository from this template

    [Creating a repository from a template](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template)

2. Start the Arduino IDE:

    ```bash
    ./run.sh
    ```

### Customization

- **Arduino packages and libraries**: Add packages and libraries to be installed in `CLI-init.sh` so that they will be installed with arduino-cli at the startup of the container.

### Start with your project

During its first execution, the Arduino-IDE initialize the environment by installing core packages. By default the IDE
is configured to save your files in the root directory `/workspace/project` which is binded with the `project` folder in your host machine. Moreover the `arduino-cli.yaml` will be an exact copy of the one inside the container, so that you can commit this configuration file in your project. Finally, the directories `~/.arduinoIDE`, `~/.arduino15` and `/workspace` are configured to be volumes associated to the container, thus their content will survive even after quitting the container unless you explicitly remove them.
