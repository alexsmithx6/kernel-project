# kernel-project
I made a kernel using Qemu because I can

## Dependencies (OS Specific):

* [Docker](https://hub.docker.com/)
* [Qemu](https://www.qemu.org/)

## Setup / Run:

1. Build the docker environment. This should take ~5 minutes:
```
docker build buildenv -t myos-buildenv
```
2. Docker environment should run. I am currently using Windows Powershell to invoke this docker environment, so I run this command:
```
docker run --rm -it -v "${pwd}:/root/env" myos-buildenv
```
3. NOTE: If running on a different OS, choose from the following commands to run as in Step 2:
    * Linux/MaxOS:
```
docker run --rm -it -v "$(pwd)":/root/env myos-buildenv
```
    * Windows Command Line:
```
docker run --rm -it -v "%cd%":/root/env myos-buildenv
```

## Resources, references, etc:
* https://github.com/davidcallanan/os-series
* https://www.youtube.com/watch?v=FkrpUaGThTQ