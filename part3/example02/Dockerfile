FROM openjdk:11 AS builder
COPY ./source /usr/src/myapp
WORKDIR /usr/src/myapp
RUN javac env1.java


FROM anapsix/alpine-java
WORKDIR /usr/src/myapp
COPY --from=builder /usr/src/myapp .
CMD ["java", "env1"]