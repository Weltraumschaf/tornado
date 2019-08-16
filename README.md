# Tornado

This is my playground for fast evaluating stuff. It is based on latest [Spring Boot][spring-boot] and a Docker [distroless image][distro-less].

To build and run execute this:

```bash
mvn clean package && java -jar target/tornado-*.jar
```

To build the Docker image execute this:

```bash
mvn clean package && docker image build -f Dockerfile -t weltraumschaf/tornado:1.0.0 target
```

To run the container execute this:

```bash
docker container run --rm -it -p 8080:8080 weltraumschaf/tornado:1.0.0
```

[spring-boot]: https://spring.io/guides/gs/spring-boot/
[distro-less]: https://github.com/GoogleContainerTools/distroless/tree/master/java
