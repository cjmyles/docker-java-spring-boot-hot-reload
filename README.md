# Docker Java Spring Boot Hot Reload Boilerplate

This repository is a starter template for developing **Java Spring Boot** applications with **hot reload** support, fully containerized with Docker and Docker Compose. It provides everything you need to quickly start building and testing REST APIs with a modern workflow.

## Features

- **Spring Boot demo project** (REST endpoint at `/hello`)
- **Dockerfile + Dockerfile.dev** for production and development builds
- **Docker Compose** setup for running the app in containers
- **Hot reload**: Change source code and instantly see updates by refreshing the endpoint
- Preconfigured Gradle build
- Includes basic `.dockerignore` and `.gitignore` files

## Quick Start

1. **Clone this repository**

```bash
git clone https://github.com/cjmyles/docker-java-spring-boot-hot-reload.git
cd docker-java-spring-boot-hot-reload
```

2. **Build & run using Docker Compose**

```bash
docker compose up --build
```

3. **Access the demo endpoint**

- Visit http://localhost:8080/hello in your browser. You should see the Hello, World! response.

4. **Hot Reload Setup**

- While the app is running, modify `src/main/java/com/example/demo/HelloWorldController.java`
- Save your changes and refresh [http://localhost:8080/hello](http://localhost:8080/hello) to see updates.

## File Structure

```text
├── Dockerfile
├── Dockerfile.dev
├── docker-compose.yaml
├── docker-compose.override.yaml
├── build.gradle
├── gradle/
│   └── wrapper/
├── src/
│   └── main/java/com/example/demo/HelloWorldController.java
├── .dockerignore
├── .gitignore
└── settings.gradle
```


## Advanced Usage

- **Run in Production**
  - Use the default `Dockerfile` for optimized production builds.
- **Run in Development Mode**
  - Use `Dockerfile.dev` for faster builds and hot reload during local development.
- **Extend Configuration**
  - Adjust Compose files or Dockerfiles as needed for your own projects.

## Troubleshooting

- Ensure Docker and Docker Compose are installed and running.
- On changes not reflecting, check that the container is using the development Dockerfile and volumes are correctly mounted.
- Check container logs for errors using:

```bash
docker compose logs
```

## Contributing

Pull requests and suggestions are welcome! Open an issue or contribute new features, improvements, or documentation.

## License

MIT