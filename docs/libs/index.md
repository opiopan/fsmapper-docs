---
sidebar_position: 1
id: lib_index
---

# Library Reference
Throughout this chapter, the libraries available for use within Lua scripts describing fsmapper's configuration will be explained.
A subset of the Lua standard libraries and libraries implementing fsmapper specific functionalities can be utilized.<br/>
This document does not delve into the Lua language specifications. Please refer to the [**Lua 5.4 Reference Manual**](https://www.lua.org/manual/5.4/) for detabils on the Lua language specifications.

## Available Lua Standard Libraries
|Name| Description|
|----|------------|
|[basic](https://www.lua.org/manual/5.4/manual.html#6.1)|Basic functions|
|[package](https://www.lua.org/manual/5.4/manual.html#6.3)|Basic facilities for loading modules|
|[string](https://www.lua.org/manual/5.4/manual.html#6.4)|String manipulation|
|[table](https://www.lua.org/manual/5.4/manual.html#6.6)|Table manipulation|
|[math](https://www.lua.org/manual/5.4/manual.html#6.7)|Mathematical functions|

## fsmapper Specific Libraries

|Name| Description|
|----|------------|
|[mapper](/libs/mapper)|fsmapper basic library|
|[filter](/libs/filter)|Native-actions capable of cascading with other actions|
|[fs2020](/libs/fs2020)|Interactivity features with Microsoft Flight Simulator|
|[graphics](/libs/graphics)|Graphics library|