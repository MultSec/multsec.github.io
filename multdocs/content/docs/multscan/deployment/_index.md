---
linkTitle: "Deployment"
weight: 3
prev: /docs/multscan/how_it_works
next: /docs/multscan/usage
title: Deployment
---

The project provides two main ways to deploy the application:

1. **Docker** (recommended): The project provides a Dockerfile that can be used to build a Docker image and run the application in a container.

2. **Manual**: The project can be deployed manually by running the application directly on the host machine.

## Docker

The project provides a Dockerfile that can be used to build a Docker image and run the application in a container. The Dockerfile is located in the root of the project and can be used to build a Docker image using the following command:

```bash
$ docker build -t multscan .
DEPRECATED: The legacy builder is deprecated and will be removed in a future release.
            Install the buildx component to build images with BuildKit:
            https://docs.docker.com/go/buildx/

Sending build context to Docker daemon  9.587MB
Step 1/7 : FROM python
 ---> 6c25da8c8f13
<SNIP>
Step 7/7 : CMD ["python3", "run.py"]
 ---> Running in cceac9e3b567
 ---> Removed intermediate container cceac9e3b567
 ---> 5b017e97052f
Successfully built 5b017e97052f
Successfully tagged multscan:latest
$
```

Once the Docker image has been built, the application can be run in a container using the following command:

```bash
$ docker run -p  8000:8000 multscan
[*] Using connector: proxmox
[*] Loaded 2 machines:
        [-] machine1 (10.10.10.10)
        [-] machine2 (10.10.10.11)
[*] Turning On Machines
```

The application will be accessible at `http://localhost:8000`.

## Manual

The project can be deployed manually by running the application directly on the host machine. The following steps can be used to deploy the application manually:

1. Install the required dependencies:

```bash
$ pip install -r requirements.txt
```

2. Run the application:

```bash
$ python3 run.py
[*] Using connector: proxmox
[*] Loaded 2 machines:
        [-] machine1 (10.10.10.10)
        [-] machine2 (10.10.10.11)
[*] Turning On Machines
```

The application will be accessible at `http://localhost:8000`.