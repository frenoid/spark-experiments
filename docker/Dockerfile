FROM spark:3.5.1-scala2.12-java17-ubuntu

USER root

RUN set -ex; \
    apt-get update; \
    apt-get install -y python3.11-full python3-pip; \
    apt-get -y remove python3.10*; \
    rm -rf /var/lib/apt/lists/*

RUN ["cp", "/usr/bin/python3.11" ,"/usr/bin/python"]

RUN ["cp", "/usr/bin/python3.11", "/usr/bin/python3"]

USER spark

ENV PYSPARK_PYTHON=/usr/bin/python3.11

ENV PYSPARK_DRIVER_PYTHON=/usr/bin/python3.11
