# API C SocialQueue.GetGroupInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_SocialQueue|system=SocialQueue}}
Retrieves information about a group in social queue.
 canJoin, numQueues, needTank, needHealer, needDamage, isSoloQueueParty, questSessionActive, leaderGUID = C_SocialQueue.GetGroupInfo(groupGUID)

==Arguments==
:;groupGUID:{{apitype|string}} - a string containing the hexadecimal representation of the player's [[GUID]]

==Returns==
:;canJoin:{{apitype|boolean}}
:;numQueues:{{apitype|number}}
:;needTank:{{apitype|boolean}}
:;needHealer:{{apitype|boolean}}
:;needDamage:{{apitype|boolean}}
:;isSoloQueueParty:{{apitype|boolean}}
:;questSessionActive:{{apitype|boolean}}
:;leaderGUID:{{apitype|string}}

==Patch changes==
* {{Patch 8.2.5|note=Added <code>questSessionActive</code> return.}}
* {{Patch 7.1.0|note=Added.}}
```