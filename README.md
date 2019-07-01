# XtreemFS-Raspbian-Buster

Install docker:
`apt-get install libltdl7`
`dpkg -i containerd.io_1.2.6-3_armhf.deb`
`dpkg -i docker-ce-cli_18.09.0~3-0~raspbian-stretch_armhf.deb`
`dpkg -i docker-ce_18.09.0~3-0~raspbian-stretch_armhf.deb`

Refer to https://github.com/xtreemfs/xtreemfs-docker for next steps, but replace any occurrences of "amd64" by "armhf" in the file https://github.com/xtreemfs/xtreemfs-docker/blob/master/xtreemfs-common/Dockerfile.

# Troubleshooting

The raspberry Pi may hang during the building step of the xtreemfs-client. This seems to occur because of a lack of memory: 1Gb of RAM + 100Mb of SWAP. A solution to this issue is to increase the SWAP memory by adding a SWAP partition.

To replace the existing SWAP by using a USB disk, assuming your USB device has one partition /dev/sda1, run `mkswap /dev/sda1` to format the USB key as SWAP.

Then `swapon /dev/sda1` activate the SWAP partition for use. Check that the partition is used by the system by running `swapon --show`.

Optionally,you can run remove the default SWAP partition allocated on the SD card: `swapoff /dev/thepartitiontobedisabled`
