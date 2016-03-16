mbentley/cs-engine-downloader
=============================

docker image to download the Docker CS engine RPMs for CentOS/RHEL 7, SUSE/SLES 12, and Ubuntu 14.04
based off of centos:7, jess/opensuse:12.3, and ubuntu:14.04

To pull this image:

apt (Ubuntu 14.04) - `docker pull mbentley/cs-engine-downloader:apt`

yum (CentOS/RHEL 7) - `docker pull mbentley/cs-engine-downloader:yum`

zypper (SUSE/SLES 12) - `docker pull mbentley/cs-engine-downloader:zypper`

Example usage:

`docker run -it --rm -v /data:/data mbentley/cs-engine-downloader:apt`

`docker run -it --rm -v /data:/data mbentley/cs-engine-downloader:yum`

`docker run -it --rm -v /data:/data mbentley/cs-engine-downloader:zypper`

By default, this downloads the DEBs or RPMs (including dependencies) to /data; this directory can be modified using the `DOWNLOAD_DIR` environment variable.

Copy the resulting DEB(s) or RPM(s) to the system to install the Docker engine and then install (replacing the DEB/RPM name appropriately):

`dpkg -i docker-engine_1.10.2~cs1-0~trusty_amd64.deb; apt-get -f install`

`yum install docker-engine-1.9.1-1.el7.centos.x86_64.rpm`

`zypper in docker-engine-1.10.0.cs1-0.1.rc1.x86_64.rpm`
