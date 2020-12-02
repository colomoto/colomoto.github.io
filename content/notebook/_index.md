---
title: "The CoLoMoTo Interactive Notebook"
hidetitle: true
date: 2020/12/02 12:58
menu: 
    nav:
        name: "Notebook"
        weight: 5
extrasections: sections
---

The CoLoMoTo Interactive Notebook relies on *Docker* and *Jupyter*
technologies to provide a **unified environment** to edit, execute, share,
and reproduce analyses of **qualitative models of biological networks**.

## Quick usage guide

### Without any installation

Visit [mybinder.org/v2/gh/colomoto/colomoto-docker/mybinder/latest](https://mybinder.org/v2/gh/colomoto/colomoto-docker/mybinder/latest) to launch the most recent CoLoMoTo Notebook environment without any installation thanks to [Binder](https://mybinder.org) services. You can replace `latest` with a specific [image tag](https://github.com/colomoto/colomoto-docker/releases).

Note that the computing resources are limited and the storage is not persistent.

### With Python Helper Script

You need [Docker](https://docs.docker.com/get-docker/) and [Python](http://python.org).
We support GNU/Linux, macOS, and Windows.

    sudo pip install -U colomoto-docker   # only once; you may have to use pip3
    colomoto-docker

The container can be stopped by pressing <kbd>Ctrl</kbd>+<kbd>C</kbd> keys.

By default, the script will fetch the most recent [colomoto/colomoto-docker tag](https://github.com/colomoto/colomoto-docker/releases). A specific tag can be specified using the `-V` option; or use `-V same` to use the most recently fetched image. For example:

    colomoto-docker                 # uses the most recently fetched image
    colomoto-docker -V latest       # fetches the latest published image
    colomoto-docker -V 2018-05-29   # fetches a specific image

**Warning**: by default, the files within the Docker container are isolated from the running host computer, therefore *files are deleted after stopping the container*, except the files within the `persistent` directory.

To have access to the files of your current directory you can use the `--bind` option:

    colomoto-docker --bind .

If you want to have the tutorial notebooks alongside your local files, you can
do the following:

    mkdir notebooks
    colomoto-docker -v notebooks:local-notebooks

in the Jupyter browser, you will see a `local-notebooks` directory which is
bound to your `notebooks` directory.

See

    colomoto-docker --help

for other options.

Having issues? have a look at our [Troubleshooting](https://github.com/colomoto/colomoto-docker/blob/master/TROUBLESHOOTING.md) page, or [open an issue](https://github.com/colomoto/colomoto-docker/issues).

### Python-less usage

You need [Docker](https://docs.docker.com/get-docker/).

First, pick an image version among [colomoto/colomoto-docker tags](https://github.com/colomoto/colomoto-docker/releases).
Fetch the image with

    docker pull colomoto/colomoto-docker:TAG

The image can be ran using

    docker run -it --rm -p 8888:8888 colomoto/colomoto-docker:TAG

then, open your browser and go to http://localhost:8888 for the Jupyter notebook web interface
(note: when using Docker Toolbox, replace localhost with the result of
`docker-machine ip default` command).


