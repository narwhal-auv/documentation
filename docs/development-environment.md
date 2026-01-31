# Development Environment

We can start working on the workspace as easy as running the docker container. A standard development environment to use by everyone for easier codes reproducibility and consistency across team member.

## Installation

1. Install Docker
3. Build the Image by calling docker compose, it will take some times. just wait until finish.

  ```bash
  docker compose -f compsoe_dev.yaml up -d
  ```
  
4. Enter the docker container

  ```bash
  docker exec -it narwhal-dev /bin/zsh
  ```
  
5. [optional] Install the ardupilot for software in the loop/ simulation
  
  ```bash
  cd narwhal_ws
  ```
  
  ```bash
  ./install_ardupilot.sh
  ```
  
  > If there are any dependencies issue, just follow the error message to know what we needs to install.
