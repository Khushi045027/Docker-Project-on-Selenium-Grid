# Selenium Standalone Chrome Docker Container

This project demonstrates the process of setting up a Selenium Standalone Chrome container using Docker. It allows you to run Selenium tests with the Chrome browser in a Docker container for an efficient and isolated testing environment.

## Prerequisites

To follow this setup, you need:

- Docker installed on your machine.
- A working internet connection to pull the Docker image.
- Basic understanding of Docker and Selenium.

## Steps to Set Up

### 1. Pull the Selenium Standalone Chrome Image

First, pull the latest `selenium/standalone-chrome` image from Docker Hub.

```bash
docker pull selenium/standalone-chrome
```

This command downloads the image containing a ready-to-use Selenium server with the Chrome browser pre-configured.

### 2. Run the Docker Container

After successfully pulling the image, you can run it as a detached container with the following command:

```bash
docker run -d -p 4444:4444 selenium/standalone-chrome
```

This command does the following:
- Runs the Selenium Standalone Chrome container in the background (`-d`).
- Maps port 4444 from the container to port 4444 on the host machine (`-p 4444:4444`), allowing you to interact with Selenium via WebDriver on this port.

### 3. Verify the Container is Running

To verify that the container is running properly, you can check the container's status by running:

```bash
docker ps
```

You should see the `selenium/standalone-chrome` container listed, confirming it is up and running.

### 4. Access Selenium WebDriver

Once the container is up and running, Selenium WebDriver will be available on `http://localhost:4444/wd/hub`. You can connect to it using your preferred programming language (Java, Python, etc.) by specifying the address `http://localhost:4444/wd/hub` as the remote WebDriver URL.


## Conclusion

This setup provides a scalable, efficient, and isolated environment for running Selenium tests with the Chrome browser using Docker. It eliminates the need to install dependencies and browsers locally and makes it easy to spin up testing environments for CI/CD pipelines or other automated testing scenarios.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
