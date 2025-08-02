# API C GamePad.SetVibration

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_GamePad|system=GamePad}}
Makes the gamepad vibrate.
 C_GamePad.SetVibration(vibrationType, intensity)

==Arguments==
:;vibrationType:{{apitype|string}} : <code>["Low", "High", "LTrigger", "RTrigger"]</code>
:;intensity:{{apitype|number}} : <code>[0.0-1.0]</code>

==Details==
* Vibration duration last for around 1 second.
* "Trigger" type vibrations appear to be only supported by the PS5 controller, as trigger haptic vibration.

==Example==
Vibrates the gamepad at 100% intensity.
 C_GamePad.SetVibration("High", 1)

==Patch changes==
* {{Patch 9.1.5|note=Added.}}

{{apinavbox|C_GamePad}}
```