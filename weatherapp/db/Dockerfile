# Use the official MySQL image from the Docker Hub
FROM mysql:8.0

# Set environment variables for MySQL configuration
ENV MYSQL_ROOT_PASSWORD=my-secret-pw

# Optional: Switch to root user for installations/configuration if needed
USER root

# Add any installation commands here, e.g., installing packages
# RUN apt-get update && apt-get install -y <your-package>

# Add a health check
HEALTHCHECK --interval=30s --timeout=10s --start-period=5s --retries=3 \
    CMD mysqladmin ping -h localhost || exit 1
