# Install Docker

## Windows

1. Download Docker Desktop for Windows from [Docker's official website](https://www.docker.com/products/docker-desktop).
2. Run the installer and follow the on-screen instructions.
3. Once the installation is complete, Docker Desktop will start automatically.
4. Verify the installation by opening a command prompt and running:
    ```sh
    docker --version
    ```

## macOS

1. Download Docker Desktop for Mac from [Docker's official website](https://www.docker.com/products/docker-desktop).
2. Open the downloaded `.dmg` file and drag the Docker icon to the Applications folder.
3. Launch Docker from the Applications folder.
4. Follow the on-screen instructions to complete the installation.
5. Verify the installation by opening a terminal and running:
    ```sh
    docker --version
    ```

## Linux

### Ubuntu

1. Update your existing list of packages:
    ```sh
    sudo apt-get update
    ```
2. Install a few prerequisite packages which let `apt` use packages over HTTPS:
    ```sh
    sudo apt-get install apt-transport-https ca-certificates curl software-properties-common
    ```
3. Add the GPG key for the official Docker repository to your system:
    ```sh
    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
    ```
4. Add the Docker repository to APT sources:
    ```sh
    sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
    ```
5. Update your package database with the Docker packages from the newly added repo:
    ```sh
    sudo apt-get update
    ```
6. Install Docker:
    ```sh
    sudo apt-get install docker-ce
    ```
7. Verify the installation by running:
    ```sh
    docker --version
    ```

### CentOS

1. Update your existing list of packages:
    ```sh
    sudo yum update
    ```
2. Install the `yum-utils` package (which provides the `yum-config-manager` utility) and set up the Docker repository:
    ```sh
    sudo yum install -y yum-utils
    sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
    ```
3. Install Docker:
    ```sh
    sudo yum install docker-ce docker-ce-cli containerd.io
    ```
4. Start Docker:
    ```sh
    sudo systemctl start docker
    ```
5. Verify the installation by running:
    ```sh
    docker --version
    ```

### Fedora

1. Update your existing list of packages:
    ```sh
    sudo dnf -y update
    ```
2. Install the `dnf-plugins-core` package and set up the Docker repository:
    ```sh
    sudo dnf -y install dnf-plugins-core
    sudo dnf config-manager --add-repo https://download.docker.com/linux/fedora/docker-ce.repo
    ```
3. Install Docker:
    ```sh
    sudo dnf install docker-ce docker-ce-cli containerd.io
    ```
4. Start Docker:
    ```sh
    sudo systemctl start docker
    ```
5. Verify the installation by running:
    ```sh
    docker --version
    ```
    ### RHEL 9

    1. Update your existing list of packages:
        ```sh
        sudo yum update
        ```
    2. Install the `yum-utils` package and set up the Docker repository:
        ```sh
        sudo yum install -y yum-utils
        sudo yum-config-manager --add-repo https://download.docker.com/linux/rhel/docker-ce.repo
        ```
    3. Install Docker:
        ```sh
        sudo yum install docker-ce docker-ce-cli containerd.io
        ```
    4. Start Docker:
        ```sh
        sudo systemctl start docker
        ```
    5. Verify the installation by running:
        ```sh
        docker --version
        ```

    ### Oracle Linux

    1. Update your existing list of packages:
        ```sh
        sudo yum update
        ```
    2. Install the `yum-utils` package and set up the Docker repository:
        ```sh
        sudo yum install -y yum-utils
        sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
        ```
    3. Install Docker:
        ```sh
        sudo yum install docker-ce docker-ce-cli containerd.io
        ```
    4. Start Docker:
        ```sh
        sudo systemctl start docker
        ```
    5. Verify the installation by running:
        ```sh
        docker --version
        ```

        ## Prerequisites

        ### Windows
        - Windows 10 64-bit: Pro, Enterprise, or Education (Build 16299 or later)
        - Hyper-V and Containers Windows features must be enabled

        ### macOS
        - macOS must be version 10.14 or newer
        - At least 4GB of RAM

        ### Linux
        - A 64-bit version of one of the following:
            - Ubuntu 18.04 or newer
            - CentOS 7 or newer
            - Fedora 30 or newer
            - RHEL 9 or newer
            - Oracle Linux 7 or newer
        - Kernel version 3.10 or newer
        - At least 2GB of RAM
        - The `sudo` command must be available
        - The `curl` command must be available
        - The `apt-get`, `yum`, or `dnf` package manager must be available
        - The `systemctl` command must be available
        - Internet connection to download Docker packages