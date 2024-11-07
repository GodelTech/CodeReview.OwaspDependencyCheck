# CodeReview.OwaspDependencyCheck

NuGet: https://hub.docker.com/r/godeltech/owasp-dependency-checker

## Description

This repository contains docker file for [Owasp dependency check](https://owasp.org/www-project-dependency-check/).
Image includes cache of National Vulnerability Database downloaded during building.

## Usage

### How to build the Docker Image

To build the Docker image, run the following commands:

```bash
docker build -t godeltech/owasp-dependency-checker:0.0.1 . 
```

### How to run the Docker Container

To run the Docker container, use the following command:

```bash
docker run -v "/d/temp:/src" -v "/d/temp2:/artifacts" -it --rm godeltech/owasp-dependency-checker --scan /src --format JSON --out /artifacts -n
```

## License

This project is licensed under the MIT License. See the LICENSE file for more details.