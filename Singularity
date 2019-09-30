Bootstrap:docker
From: ubuntu:rolling

%post

apt-get update
apt-get install -y python-setuptools cmake build-essential ninja-build python-dev libffi-dev libssl-dev python3-pip srecord gcc-arm-none-eabi
apt-get clean

pip3 install yotta
cp /version.py /usr/local/lib/python3.7/dist-packages/yotta/lib

%files

# Workaround for suppressing error: "'RegistryThingVersion' object has no attribute 'truncate'"
# See: https://github.com/ARMmbed/yotta/issues/856
version.py /

%runscript

/usr/local/bin/yotta

