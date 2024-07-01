---
linkTitle: "Deployment"
weight: 3
prev: /docs/multldr/how_it_works
next: /docs/multldr/usage
title: Deployment
---

The project provides two main ways to deploy the application:

1. **Docker** (recommended): The project provides a Dockerfile that can be used to build a Docker image and run the application in a container.

2. **Manual**: The project can be deployed manually by running the application directly on the host machine.

## Docker

The project provides a Dockerfile that can be used to build a Docker image and run the application in a container. The Dockerfile is located in the root of the project and can be used to build a Docker image using the following command:

```bash
$ docker build -t multldr .
Sending build context to Docker daemon  1.433MB
Step 1/7 : FROM python
 ---> 6c25da8c8f13
<SNIP>
Step 7/7 : CMD ["python3", "run.py"]
 ---> Using cache
 ---> c7b612640778
Successfully built c7b612640778
Successfully tagged multldr:latest
$
```

Once the Docker image has been built, the application can be run in a container using the following command:

```bash
docker run -p 5000:5000 multldr
[*] Loaded 47 plugins
```

The application will be accessible at `http://localhost:5000`.

## Manual

The project can be deployed manually by running the application directly on the host machine. The following steps can be used to deploy the application manually:

1. Install the required dependencies:

```bash
$ pip install -r requirements.txt
```

2. Install the build tools:

```bash
$ apt-get install mingw-w64 osslsigncode -y
```

3. Run the application:

```bash
$ python3 run.py
[*] Loaded 47 plugins
```

The application will be accessible at `http://localhost:5000`.