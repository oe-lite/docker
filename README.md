## OE-lite Docker repository

This repository holds the files needed for the use of Docker in the OE-lite project. The main use is for the Continuous Integration through buildbot.

## Installation

Any dockerfiles in this repository should present in the OE-lite Docker Hub as pre-built images, so you can fetch them from there. If you need to work
locally with these images, simply go to the directory holding the Dockerfile:

```
docker build -t mylocalimagename .
```

