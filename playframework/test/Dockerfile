FROM        ysihaoy/scala-play:2.12.3-2.6.2-sbt-0.13.15

RUN         apk add --update nodejs

# cache dependencies
COPY        ["build.sbt", "/tmp/build/"]
COPY        ["project/plugins.sbt", "project/build.properties", "/tmp/build/project/"]
RUN         cd /tmp/build && \
            sbt compile && \
            sbt test:compile && \
            rm -rf /tmp/build

RUN         mkdir /app

WORKDIR     /app

CMD         ["sbt"]
