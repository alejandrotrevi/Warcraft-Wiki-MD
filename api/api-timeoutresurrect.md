# API TimeoutResurrect

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=PlayerScript}}
Signals the client that an offer to resurrect the player has expired.
 TimeoutResurrect()

==Details==
* Called when the timeout timer on resurrection [[StaticPopup]]s expires. Prior to patch 5.4.0, {{api|DeclineResurrect}} was used for both timed out and declined resurrection requests.

==Patch changes==
* {{Patch 5.4.0|note=Added.}}

==See also==
* {{api|AcceptResurrect}}
* {{api|DeclineResurrect}}
```