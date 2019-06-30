# XtreemFS-Raspbian-Buster

Install docker:
`apt-get install libltdl7`
`dpkg -i containerd.io_1.2.6-3_armhf.deb`
`dpkg -i docker-ce-cli_18.09.0~3-0~raspbian-stretch_armhf.deb`
`dpkg -i docker-ce_18.09.0~3-0~raspbian-stretch_armhf.deb`

Refer to https://github.com/xtreemfs/xtreemfs-docker for next steps, but replace any occurrences of "amd64" by "armhf" in the file https://github.com/xtreemfs/xtreemfs-docker/blob/master/xtreemfs-common/Dockerfile.
