FROM mysql:8.0

# Create a user for the container
RUN useradd -ms /bin/bash appuser

# Set the user as appuser
USER appuser

# Add a health check
HEALTHCHECK --interval=30s --timeout=10s --start-period=5s --retries=3 CMD mysqladmin ping -h localhost || exit 1