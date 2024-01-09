---
sidebar_position: 11
---

# mapper.set_primary_mappings()
```lua
mapper.set_primary_mappings(mapping_defs)
```
This funcion sets up the primary Event-Action mappings.


## Prameters
|Parameter|Type|Description|
|-|-|-|
|`mapping_defs`|table|Specify an array table of [Event-Action mapping definiton](#event-action-mapping-definition)

### Event-Action mapping definition
|Parameter|Type|Description|
|-|-|-|
|`event`|numeric|Specify the event ID of the event targeted for mapping.
|`action`|function,<br/>[native-action](/guide/event-action-mapping#action)|Specify the action targeted for mapping.<br/>A Lua function or [native-action](/guide/event-action-mapping#action) can be specified as a action.


## Return Values
This function doesn't return any value.