mbentley/cs-engine-downloader
=============================

docker image to download the Docker CS engine RPMs for CentOS/RHEL 7
based off of centos:7

To pull this image:
`docker pull mbentley/cs-engine-downloader`

Example usage:
`docker run -it --rm -v /data:/data mbentley/cs-engine-downloader:latest`

By default, this downloads the RPMS (including dependencies) to /data; this directory can be modified using the `DOWNLOAD_DIR` environment variable.
