[Vesta Control Panel](http://vestacp.com/) for ARMv8 (64bits) / aarch64
==================================================

* Vesta is an open source hosting control panel.
* Vesta has a clean and focused interface without the clutter.
* Vesta has the latest of very innovative technologies.

Notes:
----------------------------
* This build was adapted for use on ARMv8 Servers, actually over [Scaleway](https://www.scaleway.com/?ref=logiqos) ARMv8 Cloud Servers (excluding c1 Cloud Server that have a 32bits ARM)
* For now only can be installed on Ubuntu 18.04 (for my limited time only builds the packages for this version), but in the next few weeks I will try to build the packages for the other versions of Ubuntu, as well as other flavors of linux available.
* It has not been tested on boards with ARMv8 (such as Raspberry PI, PINE64, or similar), it should not have problems, as I accept donations of boards to perform tests and / or adjustments.
* Support for Softaculous was removed because it requires IONCube, but there is no loader for ARMv8 to date, and that is why the vesta-ioncube and vesta-softaculous packages were removed.
* I do not consider supporting the ARMv7 processors (32bits), but I could do it through donations.
* As far as possible, I will add the scripts to build the vesta, vesta-nginx and vesta-php packages, for linux flavors that are not going to be officially supported.

How to install (2 step)
----------------------------
Connect to your server as root via SSH
```bash
ssh root@your.server
```

Download the installation script, and run it:
```bash
curl https://vesta-arm.s3.nl-ams.scw.cloud/vst-install.sh | bash
```

How to install (3 step)
----------------------------
If the above example does not work, try this 3 step method:
Connect to your server as root via SSH
```bash
ssh root@your.server
```

Download the installation script:
```bash
curl -O https://vesta-arm.s3.nl-ams.scw.cloud/vst-install.sh
```
Then run it:
```bash
bash vst-install.sh
```

License
----------------------------
Vesta-ARM is licensed under  [GPL v3 ](https://github.com/LOGIQOS/vesta-arm/blob/master/LICENSE) license

Thanks to:
----------------------------
[Serghey Rodin](https://github.com/serghey-rodin) for VESTA Control Panel code.

[Scaleway´s Object Storage](https://www.scaleway.com/betas/#anchor_objectstorage?ref=logiqos) S3 standard compliant object storage, now on free public beta, for host the installer scripts and vesta-arm package repository.
