This repository holds source scripts and tools for building a PhantomJS RPM
package. This package will also include xvfb-run, so you are good to
run your headless tests.

This cleaned repository excludes the several hundred MB of source tarballs and build 
dependency RPMs each of which can be retrieved using the fetch-phantomjs script and 
the Yum package manager respectively.

# Ingredients
- Qt 4.7: from http://dl.atrpms.net/el5-x86_64/atrpms/testing/
- xfvb-run(.sh): from xorg-x11-server-1.5.3-5.fc10.src.rpm
- xvfb init script
- PhantomJS: from http://code.google.com/p/phantomjs/

# Licenses
- Qt 4.7: LGPL
- PhantomJS: BSD
- Xorg-X11-Server: MIT

# How to prepare build environment
- yum/rpm install qt47-devel qt47-webkit qt47-webkit-devel sqlite-devel

# How to build
- Retrieve the PhantomJS source tarball for your chosen version
  using the included tool script: `fetch-phantomjs $version`
- `./rpm SPECS/phantomjs-$version.spec` taking note to update version in the top of the the specfile as needed

# Build branches
- use `fetch-phantomjs` script to fetch sources from branches
- modify .spec to suit your needs

Have fun!
Jens Braeuer (Original Author)
Colin Hill
