---
sidebar_position: 10
---

# Event Modifier modparam Parameter Specification
This section explains the structure of a table specified as `modparam` parameter when defining modifiers in [`mapper.device`](/libs/mapper/mapper_device).

## raw Modifier
There are currently no `modparam` available for specification.

## button Modifier
|Key|Type|Description|
|---|----|-----------|
|`polarity`|string|When `negative` is specified, it interprets ON/OFF inversely; the default is `positive`.
|`max_threshold`|numeric|Specify this when treating a [**Device Unit**](/guide/device#device-unit) with continuous values like a binary button.<br/>Interpreted as ON when the specified value is exceeded.
|`min_threshold`|numeric|Specify this when treating a [**Device Unit**](/guide/device#device-unit) with continuous values like a binary button.<br/>Interpreted as OFF when the specified value is undercut.
|`longpress`|numeric|Specify the value in milliseconds, it triggers a `longpressed` event when the button is held down for the specified duration
|`doubleclick`|numeric|Specify the value in milliseconds.<br/>If double-clicked within the specified time, the `doubleclicked` event is triggered. If there's no second click within the specified time after the initial click, the `singleclicked` event is triggered.
|`click_timing`|string| Specify the timing for determining clicks as `up` or `down`. The default is `down`.<br/>The default is `down`.
|`repeat_interval`|numeric|Specify the value in milliseconds. It triggers a `down` events repeatedly at specified time intervals while the button is held down.
|`repeat_delay`|numeric|Specify the time, in milliseconds, before the repeat operation begins after pressing the button. This setting is effective only when `repeat_interval` is specified.<br/>The default is `0`.
|`follow_down`|numeric|Specify the value in milliseconds. It trigers a `follow_down` event once the specified time has passed since the occurrence of a `down` event.
|`follow_up`|numeric|Specify the value in milliseconds. It trigers a `follow_up` event once the specified time has passed since the occurrence of a `up` event.

## incdec Modifier
|Key|Type|Description|
|---|----|-----------|
|`pulse_mode`|boolean|When `true` is specified, it operates in **pulse mode**. The default is `false`.<br/>**Pulse mode** generates two events, corresponding to push and release, like a button, based on the number of times the change amount is set in the `increment` or `decrement` event values.<br/>Instead of the `increment` event, it triggers the `increment_pulse` event, and for the `decrement` event, it triggers the `decrement_pulse` event. The [**Event Value**](/guide/event-action-mapping#event) sets `1` for push simulation and `0` for release simulation.
|`pulse_duration`|numeric|When in pulse mode, specify the duration of the simulated press in milliseconds.<br/>The default is `30`.
|`pulse_interval`|numeric|When in pulse mode, specify the minimum time in milliseconds between the simulated release and the next simulated press.<br/>The default is `30`.
|`max_hold_num`|numeric|Specifies the maximum number of pulse generations to hold. Setting this value too high might lead to continued event generation long after the [**Device Unit**](/guide/device#device-unit)'s change has stopped. Adjust this value based on the desired real-time responsiveness.<br/>The default is `4`.

