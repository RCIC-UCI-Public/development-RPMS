# development-RPMS
RPMS for needed to build other RPMS that are created with yaml2rpm

Generic system Preparation:  The following needs to be done on your build system (CentOS base/updates)
```
yum install wget git rpm-build environment-modules
```

The following RPMS are needed to be able to build on a vanilla CentOS 7 system
You only need to prep a build system once with these RPMS.

```
wget https://github.com/RCIC-UCI-Public/development-RPMS/blob/master/rocks-devel-7.1-10.x86_64.rpm?raw=true -O rocks-devel-7.1-10.x86_64.rpm
wget https://github.com/RCIC-UCI-Public/development-RPMS/blob/master/yaml2rpm-1.3-1.x86_64.rpm?raw=true -O yaml2rpm-1.3-1.x86_64.rpm
wget https://github.com/RCIC-UCI-Public/development-RPMS/blob/master/rcic-module-support-1.0-1.x86_64.rpm?raw=true -O rcic-module-support-1.0-1.x86_64.rpm
yum install rocks-devel*rpm yaml2rpm*rpm rcic-module-support*rpm
. /etc/profile.d/yaml2rpm.sh
. /etc/profile.d/rocks-devel.sh
. /etc/profile.d/modules.sh
```

You can then download yaml2rpm based repos and build according to their local 
instructions
