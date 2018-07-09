# mvanwinkleias_dell_inspiron_1525_lubuntu_18_mods

This wasn't intended (yet) to work as a package.  The files that were created / modified are under src/etc .

# License

copyright (C) 2017 Author, Institution

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

See 

* http://www.gnu.org/licenses/

## Description

* some_script.sh - does something.

# Supplemental Documentation

Supplemental documentation for this project can be found here:

* [Supplemental Documentation](./doc/index.md)

# Installation - TODO

I believe if built from a package the files *should* get installed, but it will wipe out any changes you have in the directories.  If you're building lots of old dell inspiron computers, then it *might* work.

Ideally stuff should run if you clone the git repo, and install the deps specified
in either "deb_control" or "rpm_specific"

Optionally, you can build a package which will install the binaries in

* /opt/IAS/bin/mvanwinkleias-dell-inspiron-1525-lubuntu-18-mods/.

# Building a Package

## Requirements

### All Systems

* fakeroot

### Debian

* build-essential

### RHEL based systems

* rpm-build

## Export a specific tag (or just the source directory)

## Supported Systems

### Debian packages

```
  fakeroot make clean install debsetup debbuild
```

### RHEL Based Systems

If you're building from a tag, and the spec file has been put
into the tag, then you can build this on any system that has
rpm building utilities installed, without fakeroot:

```
make clean install cp-rpmspec rpmbuild
```

This will generate a new spec file every time:

```
fakeroot make clean install rpmspec rpmbuild
```

