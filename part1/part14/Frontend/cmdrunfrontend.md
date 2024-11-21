# Run the Frontend: Build and start the frontend container:

```bash
docker build -t example-frontend .
docker run -d -p 5000:5000 example-frontend
```