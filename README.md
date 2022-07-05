# wazo-python-pystun3-packaging

Debian packaging for [pystun3](https://github.com/talkiq/pystun3) used in Wazo.

## Upgrading

To upgrade pystun3:

* Update the version number in the `VERSION` file
* Update the changelog using `dch -i` to the matching version
* Refresh patches
* Push the changes

## Building Locally

To build on a test environment before submitting a change to production the following procedure can be used.

```sh
make -f debian/rules get-orig-source
tar -xvf ../wazo-python-pystun3-packaging_*.orig.tar.gz  --strip 1
dpkg-buildpackage -us -uc
```
The `.deb` will be located in the parent directory.
