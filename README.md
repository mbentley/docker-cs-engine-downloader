mbentley/cs-engine-downloader
=============================

docker image to download the Docker CS engine RPMs for CentOS/RHEL 7 and SUSE/SLES 12
based off of centos:7 and jess/opensuse:12.3

To pull this image:

yum (CentOS/RHEL 7) - `docker pull mbentley/cs-engine-downloader:yum`

zypper (SUSE/SLES 12) - `docker pull mbentley/cs-engine-downloader:zypper`

Example usage:

`docker run -it --rm -v /data:/data mbentley/cs-engine-downloader:yum`

`docker run -it --rm -v /data:/data mbentley/cs-engine-downloader:zypper`

By default, this downloads the RPMs (including dependencies) to /data; this directory can be modified using the `DOWNLOAD_DIR` environment variable.

Copy the resulting RPM(s) to the system to install the Docker engine and then install (replacing the RPM name appropriately):

`yum install docker-engine-1.9.1-1.el7.centos.x86_64.rpm`

`zypper in docker-engine-1.10.0.cs1-0.1.rc1.x86_64.rpm`
