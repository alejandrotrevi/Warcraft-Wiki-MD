# API C Garrison.GetLandingPageShipmentInfoByContainerID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information on Garrison/Class Hall/other shipment in progress.
 name, texture, shipmentCapacity, shipmentsReady, shipmentsTotal, creationTime, duration, timeleftString, itemName, itemTexture, unk1, itemID, followerID = C_Garrison.GetLandingPageShipmentInfoByContainerID(containerID)

==Arguments==
:;containerID:{{apitype|number}} - Container ID as returned from C_Garrison.GetFollowerShipments or C_Garrison.GetLooseShipments.

==Returns==
:;name:{{apitype|string}} - shipment name
:;texture:{{apitype|number}} - shipment texture
:;shipmentCapacity:{{apitype|number}}
:;shipmentsReady:{{apitype|number}}
:;shipmentsTotal:{{apitype|number}}
:;creationTime:{{apitype|number}}
:;duration:{{apitype|number}}
:;timeleftString:{{apitype|string}}
:;itemName:{{apitype|string}} - name of item produced by this shipment
:;itemTexture:{{apitype|number}} : [[FileID]]
:;unk1:{{apitype|number}}
:;itemID:{{apitype|number}} - ID of item produced by this shipment
:;followerID:{{apitype|number}}

==Patch changes==
* {{Patch 7.0.3|note=Added.}}
```