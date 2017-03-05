Chisel Examples
===============

This shall be a collection of code examples for [Chisel](https://github.com/ucb-bar/chisel).

Getting the Examples
====================

    $ git clone https://github.com/hypoalex/chisel-examples.git

This is a collection of small Chisel projects.


Building with Docker
====================

These images are a bit large! I recommend Docker for Mac.

    docker pull hypoalex/riscv-chisel
    docker run -v $(pwd):/code -it hypoalex/riscv-chisel /bin/bash
    cd /code/examples
    make