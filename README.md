# WiFi_Hotspot_Ubuntu20.04

## Overview

Notes how to enable WiFi Hotspot on Ubuntu20.04 in specific IP range.

## Category

## Description

Turn on WiFi hotspot is greyed out for regular user. Need to run gnome-control-center by sudo command.

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


