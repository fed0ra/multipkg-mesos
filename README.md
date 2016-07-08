# Multipkg 

Multipkg automates and versions your package builds.

Use multipkg packaged mesos.

## Installation

Multipkg is best installed via rpms/debs built by... Multipkg.

The first step, clone multipkg via git:

```
$ git clone git@github.com:ytoolshed/multipkg.git
```

Then install `YAML::Syck` and `makemaker`:

```
# CentOS/Fedora/RHEL
$ yum install -y perl-YAML-Syck perl-ExtUtils-MakeMaker

# Ubuntu/Debian
$ apt-get install -y libyaml-syck-perl
```

cd multipkg, manually build and install your first multipkg package:

```
PREFIX=./root PKGVERID=0 INSTALLDIR=source scripts/transform
perl -I ./source/lib root/usr/bin/multipkg -t .
```

## Build Mesos

If you already have mesos source code, extract to `~/mesos/source`, then run:

```
$ multipkg -t . -v
```
