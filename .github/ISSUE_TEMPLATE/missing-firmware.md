---
name: Question
about: Ask about firmware that you think should exist in LVFS and fwupd
title: ''
labels: missing-firmware
assignees: ''

---

**Hardware Information**

Please provide the full device list and also the HwID data:

```shell
fwupdmgr get-devices --show-all-devices
sudo fwupdtool hwids
```

**fwupd version information**
Please provide the version of the daemon and client if applicable to your current installation of `fwupd`.

```shell
fwupdtool get-report-metadata
```
