# MyWebApi

This is a simple .NET 8.0 Web API project.

## Running the Application with Docker

To run the application using Docker, follow these steps:

1. Pull the Docker image:

```bash
   docker pull hoangtan1193/mywebapi
```

2. Run the Docker container:

```bash
docker run -d -p 8080:80 hoagtan1193/mywebapi
```

3. Access the API:

Open your browser or API client and navigate to `http://localhost:8080/weatherforecast` to access the default endpoint.