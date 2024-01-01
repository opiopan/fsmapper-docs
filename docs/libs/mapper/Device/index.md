---
sidebar_position: 1
id: Device_index
---

# Device object
Object representing a device.

## Properties
|Name|Description|
|-|-|
|[```Device.events```](/libs/mapper/Device/Device_events)|A table holding event IDs for each input unit|
|[```Device.upstream_ids```](/libs/mapper/Device/Device_upstream_ids)|A table holding unit IDs for each output unit|

## Methods
|Name|Description|
|-|-|
|[```Device.get_events()```](/libs/mapper/Device/Device_get_events)|Return a table holding event IDs for each input unit|
|[```Device.get_upstream_ids()```](/libs/mapper/Device/Device_get_upstream_ids)|Return a table holding unit IDs for each output unit|
|[```Device.close()```](/libs/mapper/Device/Device_close)|Close the device|
|[```Device.send()```](/libs/mapper/Device/Device_send)|Send a value to output unit|
|[```Device.sender()```](/libs/mapper/Device/Device_sender)|Create a native-action to send a value to output unit|
