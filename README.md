# development-RPMS
RPMS for needed to build other RPMS that are created with yaml2rpm

Generic system Preparation:  The following needs to be done on your build system (CentOS base/updates)
```
yum install wget git rpm-build environment-modules
```

The following RPMS are needed to be able to build on a vanilla CentOS 7 system
You only need to prep a build system once with these RPMS.
   ```
   YAMLRPM_VERSION=1.5-1
   ROCKSDEVEL_VERSION=7.1-11
   RCICMODULE_VERSION=1.0-1
   RCICMODULEPATH_VERSION=1.0-1
   wget https://github.com/RCIC-UCI-Public/development-RPMS/raw/master/rocks-devel-${ROCKSDEVEL_VERSION}.x86_64.rpm
   wget https://github.com/RCIC-UCI-Public/development-RPMS/raw/master/yaml2rpm-${YAMLRPM_VERSION}.x86_64.rpm
   wget https://github.com/RCIC-UCI-Public/development-RPMS/raw/master/rcic-module-support-${RCICMODULE_VERSION}.x86_64.rpm
   wget https://github.com/RCIC-UCI-Public/development-RPMS/raw/master/rcic-module-path-${RCICMODULEPATH_VERSION}.x86_64.rpm
   yum -y install rocks-devel-${ROCKSDEVEL_VERSION}.x86_64.rpm yaml2rpm-${YAMLRPM_VERSION}.x86_64.rpm rcic-module-support-${RCICMODULE_VERSION}.x86_64.rpm rcic-module-path-${RCICMODULEPATH_VERSION}.x86_64.rpm zlib-devel redhat-lsb environment-modules
   . /etc/profile.d/rocks-devel.sh
   . /etc/profile.d/yaml2rpm.sh
   . /etc/profile.d/rcic-modules.sh
   ```
You can then download yaml2rpm based repos and build according to their local 
instructions
