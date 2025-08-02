# API C SocialQueue.GetConfig

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Needs summary.
 config = C_SocialQueue.GetConfig()

==Returns==
:;config:structure - SocialQueueConfig
{| class="sortable darktable zebra"
! Field !! Type !! Description
|-
| TOASTS_DISABLED || {{apitype|boolean}} || 
|-
| TOAST_DURATION || {{apitype|number}} || 
|-
| DELAY_DURATION || {{apitype|number}} || 
|-
| QUEUE_MULTIPLIER || {{apitype|number}} || 
|-
| PLAYER_MULTIPLIER || {{apitype|number}} || 
|-
| PLAYER_FRIEND_VALUE || {{apitype|number}} || 
|-
| PLAYER_GUILD_VALUE || {{apitype|number}} || 
|-
| THROTTLE_INITIAL_THRESHOLD || {{apitype|number}} || 
|-
| THROTTLE_DECAY_TIME || {{apitype|number}} || 
|-
| THROTTLE_PRIORITY_SPIKE || {{apitype|number}} || 
|-
| THROTTLE_MIN_THRESHOLD || {{apitype|number}} || 
|-
| THROTTLE_PVP_PRIORITY_NORMAL || {{apitype|number}} || 
|-
| THROTTLE_PVP_PRIORITY_LOW || {{apitype|number}} || 
|-
| THROTTLE_PVP_HONOR_THRESHOLD || {{apitype|number}} || 
|-
| THROTTLE_LFGLIST_PRIORITY_DEFAULT || {{apitype|number}} || 
|-
| THROTTLE_LFGLIST_PRIORITY_ABOVE || {{apitype|number}} || 
|-
| THROTTLE_LFGLIST_PRIORITY_BELOW || {{apitype|number}} || 
|-
| THROTTLE_LFGLIST_ILVL_SCALING_ABOVE || {{apitype|number}} || 
|-
| THROTTLE_LFGLIST_ILVL_SCALING_BELOW || {{apitype|number}} || 
|-
| THROTTLE_RF_PRIORITY_ABOVE || {{apitype|number}} || 
|-
| THROTTLE_RF_ILVL_SCALING_ABOVE || {{apitype|number}} || 
|-
| THROTTLE_DF_MAX_ITEM_LEVEL || {{apitype|number}} || 
|-
| THROTTLE_DF_BEST_PRIORITY || {{apitype|number}} || 
|}

==Patch changes==
* {{Patch 7.1.0|note=Added.}}
```