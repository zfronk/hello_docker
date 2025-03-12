# Hello Docker Console App

This is a simple C# console application designed for learning purposes to get familiar with Docker. The application outputs two messages to the console.

## Features
- Prints "Hey there" to the console.
- Prints "Am learning Docker!" to the console.

## Prerequisites

Before running the application, make sure you have the following installed:

- **Docker**: To containerize and run the application in Docker.
- **.NET SDK**: To build and run the application locally if desired.

## Getting Started

Follow these steps to run the application locally and in Docker:

### Running Locally

1. Clone this repository to your local machine.
2. Open the solution in Visual Studio or your preferred C# IDE.
3. Build and run the application.
4. You should see the output:
   ```
   Hey there
   Am learning Docker!
   ```

### Running with Docker

1. Make sure Docker is installed and running.
2. Navigate to the directory containing your `Dockerfile`.
3. Build the Docker image:
   ```bash
   docker build -t hello-docker .
   ```
4. Run the Docker container:
   ```bash
   docker run hello-docker
   ```

You should see the same output as running the application locally:
```
Hey there
Am learning Docker!
```

## Dockerfile

The provided Dockerfile is used to build and run the application in a Docker container.

- **Base Image**: The application uses a .NET runtime image (`mcr.microsoft.com/dotnet/runtime:9.0`).
- **Build Stage**: The application is built using the .NET SDK image (`mcr.microsoft.com/dotnet/sdk:9.0`).
- **Publish Stage**: The application is published and prepared for running in a container.
- **Final Image**: The published application is copied into the final Docker image and is set to run using `dotnet Hello Docker.dll`.

## License

This project is open-source and available under the [MIT License](LICENSE).

---

Feel free to adjust or expand on any sections based on your project's needs!
