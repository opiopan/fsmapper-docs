---
sidebar_position: 1
---

# Tutrial

## Your first configuration file

```lua {3-11} title="tutrial1.lua" showLineNumbers
local my_event = mapper.register_event('My Event')
mapper.set_primary_mappings{
    {
        event = my_event,
        action = function (evid, value)
            mapper.print('Value: ' .. value)
            mapper.delay(2000, function ()
                mapper.raise_event(my_event, value + 1)
            end)
        end
    }
}
mapper.raise_event(my_event, 1)
```

## Start App to Observe events

## Handle a device

```lua {4} title="tutrial2.lua" showLineNumbers
device = mapper.device{
    name = 'Tutrial',
    type = 'dinput',
    identifier = {index = 1},
    modifiers = {},
}
```

```lua
modifiers = {
    {class = 'binary', modtype = 'button'},
}
```

## Interact with FS2020

```lua {9-22} title="tutrial3.lua" showLineNumbers
device = mapper.device{
    name = 'Tutrial',
    type = 'dinput',
    identifier = {index = 1},
    modifiers = {
        {class = 'binary', modtype = 'button'},
    }
}
local events = device:get_events()

mapper.set_primary_mappings{
    {
        event = events.button1.down,
        action = function ()
            fs2020.mfwasm.execute_rpn('')
        end
    },
    {
        event = events.button2.down,
        action = fs2020.mfwasm.rpn_executer('')
    },
}
```
