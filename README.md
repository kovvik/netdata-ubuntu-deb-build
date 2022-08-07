# netdata-ubuntu-deb-build

Tool to build ubuntu packages for Netdata using Vagrant

## Requirements
* Vagrant installed

## Usage

```
git clone https://github.com/kovvik/netdata-ubuntu-deb-build.git
cd netdata-ubuntu-deb-build
mkdir netdata_package
vagrant up --provision
```
After deb package build it will install the Netdata package to the VM and can be accessed on port 19999: http://localhost:19999
Built packages will be copied to `netdata_package` dir.

## Ubuntu and Netdata versions

Ubuntu and Netdata versions can be overriden by env variables:
```
UBUNTU_VERSION=1804 NETDATA_VERSION=1.35.0 vagrant up --provision
```
