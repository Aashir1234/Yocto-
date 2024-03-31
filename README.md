- [Getting Starting with Yocto Project](#Installing-Yocto-and-Building-first-image)
- [Understanding Local.conf](#Understanding-local.conf-syntax)


### Installing Yocto and Building first Image
## what is yocto?
THE YOCTO PROJECT. IT'S NOT AN EMBEDDED LINUX DISTRIBUTION, IT CREATES A CUSTOM ONE FOR YOU.
https://www.yoctoproject.org/
## Setup Host PC
### Install required packages
```
sudo apt install gawk wget git diffstat unzip texinfo gcc build-essential chrpath socat cpio python3 python3-pip python3-pexpect xz-utils debianutils iputils-ping python3-git python3-jinja2 libegl1-mesa libsdl1.2-dev pylint3 xterm python3-subunit mesa-common-dev zstd liblz4-tool

```
## Building Image
### What is Poky?
Poky is a reference distribution of the Yocto Project®. It contains the OpenEmbedded Build System (BitBake and OpenEmbedded Core) as well as a set of metadata to get you started building your own distro
### Cloning Poky by Kirkstone branch
```
git clone git://git.yoctoproject.org/poky -b kirkstone
```
### nitialize Build Environment
```
cd poky
source oe-init-build-env
```
## Make Changes in local.conf


=> Change Machine

=> Change source path

=> Set following

        RM_OLD_IMAGE = "1"

        INHERIT += "rm_work"

=> Save

### Build Image
#### Execute the following command from build folder
```
bibake core-image-full-cmdline
```
### Image File
Go to the tmp folder, my tmp folder is in my source folder, that we created before
```
cd ../../sources/tmp/deploy/images/beaglebone-yocto
```

### Understanding local.conf syntax
