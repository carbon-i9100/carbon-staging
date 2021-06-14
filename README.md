# Carbon Staging for i9100 #

### Sync ###

```bash

# Initialize local repository
$ repo init -u https://github.com/CarbonROM/android.git -b cr-8.0

# Clone my local repo
$ git clone https://github.com/carbon-i9100/carbon-staging.git -b primary .repo/local_manifests

# Sync
$ repo sync -c --force-sync --no-clone-bundle --no-tags
```

### Build ###

```bash
# Set up environment
 $ . build/envsetup.sh

# Generate configuration of device
 $ lunch carbon_i9100-userdebug

# Generate ramdisk
 $ mka ramdisk && cout && gunzip -c ramdisk.img > ramdisk.cpio && cd ../../../..

# Build the code
 $ make carbon
 ```
