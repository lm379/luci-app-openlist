# luci-app-openlist - for openwrt-18.06

A file list program that supports multiple storage.

## How to build

- Install `libfuse` development package.

  - ubuntu/debian:
    ```shell
    sudo apt update
    sudo apt install libfuse-dev
    ```

  - redhat:
    ```shell
    sudo yum install fuse-devel
    ```

  - arch:
    ```shell
    sudo pacman -S fuse2
    ```

- Enter in your openwrt dir

- Openwrt official SnapShots

  *1. requires golang 1.22.x or latest version (Fix build for older branches of OpenWrt.)*
  ```shell
  rm -rf feeds/packages/lang/golang
  git clone https://github.com/sbwml/packages_lang_golang -b 23.x feeds/packages/lang/golang
  ```

  *2. get luci-app-openlist source & building*
  ```shell
  git clone https://github.com/lm379/luci-app-openlist -b lua package/openlist
  make menuconfig # choose LUCI -> Applications -> luci-app-openlist
  make package/openlist/luci-app-openlist/compile V=s # build luci-app-openlist
  ```

--------------

![](https://user-images.githubusercontent.com/16485166/190462187-5d54725e-1d9b-45f3-854f-403b882fb223.png)
