Docker files for ASPECT
=======================

dealii-docker-files/ - Docker images for deal.II and other dependencies
docker-aspect-tester-8.4.1/ - Docker image used by the automated tester (does not contain ASPECT)

Instructions for the ASPECT tester
----------------------------------

cd to your local source directory and run:

    mkdir log
    docker run --rm -e BUILDS=gcc --rm -v "$(pwd):/source:ro" -v "$(pwd)/log/:/home/bob/log/"  tjhei/aspect-tester-8.4.1
