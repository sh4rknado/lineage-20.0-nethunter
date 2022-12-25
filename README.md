# lineage-20.0-nethunter
lineage-20.0 nethunter (3.0)

Building Nethunter OS from latest lineage OS for samsung S8 (exynos) (SMG950F).

## Install dependency

### install repo tools

    curl https://storage.googleapis.com/git-repo-downloads/repo > repo
  
    chmod a+x repo
  
    sudo mv repo /usr/bin/repo


### Get the source code

this command can be take +/- 2h take one or more cofee :)

    repo init -u https://github.com/LineageOS/android.git -b lineage-20.0

    repo sync


### local manifest

    mkdir -pv .repo/local_manifests/
  
  
Add the roomservice (all sources code for your specific device)

  nano .repo/local_manifests/roomservice.xml
  
  <?xml version="1.0" encoding="UTF-8"?>
  <manifest>

      <remote name="vendor"
              fetch="https://github.com"
              revision="lineage-20.0" />

      <remote name="device"
              fetch="https://github.com"
              revision="lineage-20.0"/>

      <remote name="kernel"
              fetch="https://github.com"
              revision="lineage-20.0"/>

    <project name="TheMuppets/proprietary_vendor_samsung" path="vendor/samsung" remote="vendor"/>
    <project name="LineageOS/android_device_samsung_hero2lte" path="device/samsung/dreamlte" remote="device" />
    <project name="LineageOS/android_hardware_samsung" path="hardware/samsung" remote="github" />
    <project name="LineageOS/android_kernel_samsung_universal8895" path="kernel/samsung/universal8895" remote="kernel" />
  </manifest>


## Ressources
  
- portage : https://medium.com/@daltonfury42/building-lineageos-for-your-device-a7d26ab50549

- building : https://wiki.lineageos.org/devices/gts28vewifi/build
