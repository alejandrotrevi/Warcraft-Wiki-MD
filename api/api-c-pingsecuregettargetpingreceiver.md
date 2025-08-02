# API C PingSecure.GetTargetPingReceiver

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_PingSecure|system=PingManager}} {{restrictedapi|protected}}
Returns the first suitable frame that may intercept a ping that can be found at the given screen position.
 frame = C_PingSecure.GetTargetPingReceiver(mousePosX, mousePosY)

==Arguments==
:;mousePosX:{{apitype|number}}
:;mousePosY:{{apitype|number}}

==Returns==
:;frame:{{apitype|ScriptRegion}}

==Details==
* This function will typically be supplied the return values of {{api|GetCursorPosition}}.
* This function will return the first frame in the frame stack that meet either of the following criteria:
** Any frame that is both marked as top level ({{api|t=w|Frame:SetToplevel}}) and does '''not''' have the <code>ping-top-level-pass-through</code> attribute set.
** Any frame that has the <code>ping-receiver</code> attribute set.
* When determining if an attribute is set, this function only checks if the attribute has a non-nil value. Notably, this means that setting either of these attributes to false will still result in the attribute being considered as set.
* The behavior of this function if it encounters a frame that meets a mutually exclusive set of criteria should be considered undefined. However, currently if a frame is both marked as top level and has the <code>ping-top-level-pass-through</code> attribute set then the <code>ping-receiver</code> attribute will be ignored and the frame will not be returned.

==Patch changes==
* {{Patch 10.1.7|note=Added.}}
```