FROM mysql:8.0

# Set environment variables for MySQL configuration
ENV MYSQL_ROOT_PASSWORD=my-secret-pw


# Switch to root user for installations/configuration
USER root


# Add a health check
HEALTHCHECK --interval=30s --timeout=10s --start-period=5s --retries=3 \
  CMD mysqladmin ping -h localhost || exit 1

# Switch back to the default MySQL user
USER mysql

# Add metadata labels for better documentation
LABEL version="1.0"
LABEL description="Custom MySQL 8.0 image with initialization scripts and health check"

# Documentation for usage
# This Dockerfile sets up a MySQL server with initialization scripts.