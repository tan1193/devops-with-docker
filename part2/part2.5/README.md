```bash
# Clone the repository
git clone https://github.com/docker-hy/material-applications.git
cd material-applications/scaling-exercise

# Start the application
docker-compose up

# Scale the compute containers
docker-compose up --scale compute=3
```