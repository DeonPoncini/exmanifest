---
Title: exmanifest
Description: Example manifest file
Author: Deon Poncini

---
scripts
===============

Developed by Deon Poncini <dex1337@gmail.com>

Downloads
---------
[github](https://github.com/DeonPoncini/exmanifest)

Description
-----------
This example manifest is useful for testing out the scripts build system.
This manifest checks out the exdownstream, libexupstream1 and libexupstream2
projects, that are built with the build system.

To test them, first clone the scripts repository, then you can configure the
exconfig project. Following this it will check out this manifest file, and
sync the projects which can then be built

Building
--------

    mkdir projects
    cd projects
    git clone git@github.com:DeonPoncini/scripts.git
    export PROJECT_NAME=exconfig
    touch scripts/user/user.sh
    echo '#!/bin/bash' >> scripts/user/user.sh
    echo 'export MANIFEST_GIT="git@github.com:DeonPoncini/exmanifest.git"' >> scripts/user/user.sh
    echo 'export MANIFEST_DIR="manifest"' >> scripts/user/user.sh
    source scripts/open-project.sh
    project-vcs clone
    build

Usage
-----
See build help and project-vcs help

License
-------
Copyright (c) 2014 Deon Poncini.
See the LICENSE file for license rights and limitations (MIT)
