# Python Cybersecurity Project

This project contains Python exercises focused on cybersecurity. It uses a Docker container to provide an isolated environment with the necessary dependencies.

## Getting Started with Docker

### Prerequisites

Make sure you have [Docker](https://www.docker.com/get-started) installed on your machine.

### Building the Docker Image

1. Clone or download this repository to your local machine.

2. Open a terminal or command prompt and navigate to the project directory.

3. Build the Docker image by running the following command:

   ```bash
   docker build -t python-cybersecurity -f docker/Dockerfile .
   ```
This will create a Docker image named python-cybersecurity.

### Running the Docker Container
Once the image is built, you can run the container with:

```bash
  docker run -it python-cybersecurity
```
This will start the container and execute the default Python script (your_script.py).

### Customizing the Python Script
If you want to run a specific Python script other than the default one, you can modify the CMD in the Dockerfile or run a different script manually after entering the container:

Start the container in interactive mode:

```bash
  docker run -it python-cybersecurity /bin/bash
```
Once inside the container, run the desired Python script:

```bash
  python your_script.py
```
Installing Additional Dependencies
If you need to install additional Python packages, modify the requirements.txt file and rebuild the Docker image:

```bash
  docker build -t python-cybersecurity .
```
Stopping and Removing the Container
To stop the container, simply exit the interactive session or press Ctrl + C. To remove the container, run:

```bash
  docker rm <container_id>
```
Where <container_id> is the ID of the running container, which you can find by running docker ps.
