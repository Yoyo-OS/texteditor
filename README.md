# Text Editor

Elegant text editor for YoyoOS. 

[![Build](https://github.com/Yoyo-OS/texteditor/actions/workflows/build.yml/badge.svg)](https://github.com/Yoyo-OS/texteditor/actions/workflows/build.yml)

![screenshot](screenshots/Screenshot_20211221_212801.png)

## Dependencies

### Debian/Ubuntu

```
sudo apt install equivs curl git devscripts lintian build-essential automake autotools-dev --no-install-recommends

sudo mk-build-deps -i -t "apt-get --yes" -r
```

## Build

```shell
mkdir build
cd build
cmake -DCMAKE_INSTALL_PREFIX:PATH=/usr ..
make
```

## Install

```shell
sudo make install
```

## License

This project has been licensed by GPLv3.
