BootStrap: docker
From: centos:centos7

%post
yum -y update && yum -y upgrade
yum -y install libX11-devel mesa-libGL-devel xz curl PyQt4 xkeyboard-config libXcomposite-devel

mkdir -p /opt/calibre
curl https://download.calibre-ebook.com/3.48.0/calibre-3.48.0-x86_64.txz| xzcat | tar -C /opt/calibre -xf - && /opt/calibre/calibre_postinstall

systemd-machine-id-setup 

# specific to my setup
mkdir -p /local-storage /mnt/beegfs /baycells/home /baycells/scratch /c6/shared /c6/eb /local/gensoft2 /c6/shared/rpm /Bis/Scratch2 /mnt/beegfs

%runscript
PATH=/opt/calibre/:${PATH}
export PATH
LANG=C /opt/calibre/calibre "$@"

