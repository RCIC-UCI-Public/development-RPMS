# development-RPMS
RPMS for development - small in size
These can be downloaded and then installed on a vanilla CentOS 7 system
You only need to prep a build system once with these RPMS.

```
wget https://github.com/RCIC-UCI-Public/development-RPMS/blob/master/rocks-devel-7.1-10.x86_64.rpm?raw=true -O rocks-devel-7.1-10.x86_64.rpm
wget https://github.com/RCIC-UCI-Public/development-RPMS/blob/master/yaml2rpm-1.2-1.x86_64.rpm?raw=true -O yaml2rpm-1.2-1.x86_64.rpm
wget https://github.com/RCIC-UCI-Public/development-RPMS/blob/master/rcic-module-support-1.0-1.x86_64.rpm?raw=true -O rcic-module-support-1.0-1.x86_64.rpm
yum install rocks-devel*rpm yaml2rpm*rpm rcic-module-support*rpm
. /etc/profile.d/yaml2rpm.sh
```

You can then download yaml2rpm based repos and build according to their local 
instructions
