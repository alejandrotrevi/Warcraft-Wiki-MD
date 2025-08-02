# API C SocialQueue.GetGroupQueues

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Needs summary.
 queues = C_SocialQueue.GetGroupQueues(groupGUID)

==Arguments==
:;groupGUID:{{apitype|string}}

==Returns==
:;queues:structure - SocialQueueGroupQueueInfo[]
{| class="sortable darktable zebra"
! Field !! Type !! Description
|-
| clientID || {{apitype|number}} || 
|-
| eligible || {{apitype|boolean}} || 
|-
| needTank || {{apitype|boolean}} || 
|-
| needHealer || {{apitype|boolean}} || 
|-
| needDamage || {{apitype|boolean}} || 
|-
| isAutoAccept || {{apitype|boolean}} || 
|-
| queueData || unknown QueueSpecificInfo|| 
|}

==Patch changes==
* {{Patch 7.1.0|note=Added.}}
```