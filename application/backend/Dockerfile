FROM python:3.14-slim-trixie
COPY --from=ghcr.io/astral-sh/uv:0.13.6 /uv /uvx /bin/

# Copy the project into the image
COPY . /app

# Disable development dependencies
ENV UV_NO_DEV=1

# Sync the project into a new environment, asserting the lockfile is up to date
WORKDIR /app
RUN uv sync --locked

# Use --no-sync flag, because we already set environment in previous step
CMD ["uv", "run", "--no-sync", "fastapi", "run", "--host", "0.0.0.0", "--port", "8080"]
