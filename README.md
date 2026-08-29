Klee Kernel Building
===========

Getting started
---------------

To get started with Android, you'll need to get familiar with [Source Control Tools](https://source.android.com/setup/develop).

To initialize your local repository using the Google kernel manifest, use a command like this:
```
repo init -u https://android.googlesource.com/kernel/manifest -b common-android15-6.6-2025-09 --depth=1
```
Then use a command like this to clone the local manifest at the root of your local repository:
```
git clone https://github.com/xiaomi-klee-devs/android_manifest .repo/local_manifests -b kernel/lineage-23.2
```
Then to sync up:
```
repo sync --no-clone-bundle --no-tags -j"$(nproc --all)"
```

Building the kernel
-------------------
To build the GKI kernel image and the device kernel modules, use a command like this at the root of your local repository:
```
./kernel_device_modules-6.6/build.sh
```
Then every built artifacts are available at:
```
out/dist/
```
