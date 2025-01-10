# Dockerized Node.js Application

This project demonstrates how to dockerize a simple Node.js application. Dockerization creates a Docker image that packages the application along with its dependencies, making it portable and consistent across different environments.

---

## Prerequisites

- **Node.js**: Installed locally for testing the application before containerization.
- **Docker**: Installed to run and manage Docker containers.

## Getting Started

1. **Clone the repository** to your local machine:

   ```bash
   git clone https://github.com/SHUHAIB-T/docker-node.git
   cd docker-node
   ```

2. **Install the dependencies** for the Node.js application:

```bash
npm install
```

## Dockerizing the Application

1.  **Build the Docker Image**
    To create the Docker image for this application, run the following command:

    ```bash
    docker build -t docker-node .
    ```

2.  **Run the Docker Container**
    Start a Docker container from the image, mapping port 8000 of the container to port 8000 on your local machine:
    `bash
docker run -p 8000:8000 docker-node
`
    After running this command, the application will be accessible at http://localhost:8000. You should see a message confirming that the app is running.

## Testing the Application

You can test the application using `Postman` or `cURL`.

### Example cURL Request

Use the following command to send a POST request to the application:

```bash
curl --location 'http://localhost:8000/test' \
--header 'content-type: application/json' \
--data '{
	"msg": "testing6"
}'

```

## Notes

- Make sure that port `8000` is available on your machine before running the container.
- The Dockerfile provided in this project is configured to copy only the necessary files to the Docker image, keeping it lightweight.

### Enjoy working with Dockerized applications!
