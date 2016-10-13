FROM            ubuntu:14.04.4

RUN             \
                apt-get update && \
                apt-get install -y software-properties-common && \
                add-apt-repository ppa:openjdk-r/ppa -y && \
                apt-get update && \
                apt-get install -y --no-install-recommends openjdk-8-jre && \
                rm -rf /var/lib/apt/lists/*

ADD             target/universal/stage /opt/app

EXPOSE          9000

