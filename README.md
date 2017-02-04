Docker files for ASPECT
=======================

dealii-docker-files/ - Docker images for deal.II and other dependencies
docker-aspect-tester-8.4.1/ - Docker image used by the automated tester (does not contain ASPECT)
docker-aspect-test/ - Docker image with a current ASPECT version compiled and ready to use

ASPECT Demo
----------------------------------

docker pull tjhei/aspect-demo
docker run --rm -it -v "$(pwd):/home/bob/data" tjhei/aspect-demo

Instructions for the ASPECT tester
----------------------------------

cd to your local source directory and run:

    mkdir log
    docker run --rm -e BUILDS=gcc -v "$(pwd):/source:ro" -v "$(pwd)/log/:/home/bob/log/"  tjhei/aspect-tester-8.4.1
