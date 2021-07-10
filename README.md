# WiFi_Hotspot_Ubuntu20.04

## Overview

Notes how to enable WiFi Hotspot on Ubuntu20.04 in specific IP range.

## Category

## Description

Turn on WiFi hotspot is greyed out for regular user. Need to run gnome-control-center by sudo command.
![turn_on_wifi_hotspot_greyedout](https://user-images.githubusercontent.com/9047935/125162775-abf91700-e1c4-11eb-837b-3e6a51184612.jpg)

![turn_on_wifi_hotspot_greyedout_policy](https://user-images.githubusercontent.com/9047935/125162774-ab608080-e1c4-11eb-8f88-e0b7cd539288.jpg)


Edit line containg [ipv4]

`sudo vim /etc/NetworkManager/system-connections/Hotspot.nmconnection`

add following for the IP range 192.168.0.1/24

address1=192.168.0.1/24,192.168.0.1

Save it.

Stop network manager

`sudo systemctl stop NetworkManager.service`

Start network manager

`sudo systemctl start NetworkManager.service`

Open gnome-control-center by

`sudo gnome-control-center`

Go to WiFi

Now you can select

"Turn on WiFi hotspot"

![turn_on_wifi_hotspot_available](https://user-images.githubusercontent.com/9047935/125162760-a1d71880-e1c4-11eb-854f-4f48e4641666.jpg)

## Demo in Animation

## Requirements

Internet connection (Ethernet) <-- Main connection.

## Install

## Usage

## Contributions

## Updates

## Memo

## Feature upgrades

## ToDo

## Licence
[MIT]

## Author

[linuxkay](https://github.com/linuxkay)


