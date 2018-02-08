# Include the F-Droid release binary in Custom ROMs

Download F-Droid prebuilt APKs for inclusion in a custom ROM.  This
also downloads the GPG armor files of the packages to verify them. The
signing key info can be found here:
<https://f-droid.org/docs/Release_Channels_and_Signing_Keys/>

Getting the packages
--------------------

* Add it to your local manifest:
```xml
<?xml version="1.0" encoding="UTF-8"?>
<manifest>
    <!-- F-Droid -->
    <project name="fdroid/android_vendor_fdroid"
 path="vendor/fdroid"
 remote="gitlab"
 revision="master" />
</manifest>
```

* After downloading to to the vendor dir and get the packages:
```console
$ cd vendor/fdroid
$ ./get_packages.sh
```
