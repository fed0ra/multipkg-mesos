# Multipkg 

Multipkg automates and versions your package builds.

### Installation

Multipkg is best installed via rpms/debs built by... Multipkg.

1.Install your developer tools

```
$ yum -y groupinstall "Development Tools"
```

2.install YAML::Syck and makemaker  
centos:  
```
$ yum install -y perl-YAML-Syck perl-ExtUtils-MakeMaker
```  
ubuntu:  
```
$ apt-get install -y libyaml-syck-perl
```

3.clone multipkg via git

```
$ git clone git@github.com:ytoolshed/multipkg.git  
$ cd multipkg/
```

4.manually build and install your first multipkg package

```
$ PREFIX=./root PKGVERID=0 INSTALLDIR=source scripts/transform  
$ perl -I ./source/lib root/usr/bin/multipkg -t .  
$ yum -y install multipkg-*rpm  
$ multipkg --help
```
# Mesos
### Get mesos source code
Get mesos source code, extract to `~/mesos/source`

```
$ git clone https://github.com/fed0ra/multipkg-mesos.git  
$ cd multipkg-mesos/  
$ mkdir source  
$ cd source  
$ wget http://mirror.bit.edu.cn/apache/mesos/0.28.2/mesos-0.28.2.tar.gz  
$ tar -zxf mesos-0.28.2.tar.gz --strip-component=1  
$ rm -rf mesos-0.28.2.tar.gz  
$ cd ..
```
### Build Mesos
Add executable permissions to build script

```
$ chmod +x scripts/build
```

and then run:

```
$ multipkg -t . -v
```