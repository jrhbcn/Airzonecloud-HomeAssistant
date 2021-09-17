# Please add Issue tab to your project, as i want to use your project but i have errors. THX <3


# Airzone Local plugin for Home Assistant


THIS IS A WORK IN PROGRESS AND NOT CURRENTLY WORKING. Use https://github.com/gpulido/homeassistant-airzone instead.


## Introduction

Allow to view & control all your zones register on your Airzone Local ([airzonecloud.com](https://airzonecloud.com)) system from [Home Assistant](https://www.home-assistant.io/).

This is a (heavily changed) fork from https://github.com/max13fr/Airzonecloud-HomeAssistant, if you cannot or do not want to use the local api use max13fr integration. 

![Screenshot](screenshot.png)

## Install / upgrade

### Add module

In your home assistant directory (where you have your **configuration.yaml**) :

- create the directory **custom_components** if not already existing
- copy **custom_components/airzone_local** directory from this github repository inside your **custom_components**. In case of upgrade, you can delete the **airzone_local** first then copy the new one.

Finally, you should have the following tree :

- configuration.yaml
- custom_components/
  - airzone_local/
    - \_\_init\_\_.py
    - climate.py
    - const.py
    - manifest.py

### Configure

In your **configuration.yaml** add the following lines :

```
climate:
  - platform: airzone_local
    ip: IP of local airzone server
    scan_interval: 30
```
