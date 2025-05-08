# Build Command Line

```
docker build . --tag=universal-persistent
```

# Run command Line

```
docker run -it --name powershelluniversal --mount source=psudata,target=/home/data --rm -d  -p 5000:5000/tcp universal-persistent:latest
```

## Volume Mount
The `--mount source=psudata,target=/home/data` parameter creates a persistent Docker volume named `psudata` that is mounted to `/home/data` in the container. This ensures data persists between container restarts.

# Resources

[Create a persistent docker image of PowerShell Universal](https://ironmansoftware.com/training/powershell-universal/installation-docker)
[Introduction to GitHub Actions with Docker](https://docs.docker.com/guides/gha/)
[Create an access token](https://docs.docker.com/security/for-developers/access-tokens/#create-an-access-token)