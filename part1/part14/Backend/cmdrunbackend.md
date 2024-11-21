# Run the Backend: Build and start the backend container:

```bash
docker build -t example-backend .
docker run -d -p 8080:8080 example-backend
```