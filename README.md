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


### Add roomservice (all sources code for your specific device)
    
    mkdir -pv .repo/local_manifests/
    
    wget https://github.com/sh4rknado/lineage-20.0-nethunter/blob/main/roomservice.xml
    
    cp roomservice.xml .repo/local_manifests/roomservice.xml
    
    repo sync
    

## Ressources
  
- portage : https://medium.com/@daltonfury42/building-lineageos-for-your-device-a7d26ab50549

- building : https://wiki.lineageos.org/devices/gts28vewifi/build

- Forked Source : https://github.com/8890q (android device, kernel)
