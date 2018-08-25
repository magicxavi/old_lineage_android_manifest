LineageOS 16.0
==============

Getting Started
---------------

To initialize your local repository using the LineageOS trees, use a command like this:

    $ repo init -u git://github.com/LineageOS/android.git -b lineage-16.0
    $ mkdir -p .repo/local_manifests
    $ wget https://gist.githubusercontent.com/TheStrechh/530507ff9c76d8d7675d4b594a5688f9/raw/09ad51b7c4855ad07bdae7a450879878729c845b/kenzo.xml -O .repo/local_manifests/roomservice.xml

Then to sync up:

    $ repo sync --force-sync -q -j8


Building for Xiaomi Redmi Note 3 (kenzo/kate)
---------------

To build:

    $ . build/envsetup.sh
    $ lunch lineage_kenzo-eng
    $ make bacon -j8

Building for Xiaomi Redmi 4A/5A (rolex/riva)
---------------

To build:

    $ . build/envsetup.sh
    $ lunch lineage_rolex-eng
    $ make bacon -j8
