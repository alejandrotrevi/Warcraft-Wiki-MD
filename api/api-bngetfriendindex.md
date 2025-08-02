# API BNGetFriendIndex

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Returns the index in the friend frame of the given Battle.net friend.

 index = BNGetFriendIndex(presenceID)

==Arguments==
:;presenceID:{{apitype|number}} - A unique numeric identifier for the friend's battle.net account during this session.

==Returns==
:;index:{{apitype|number}} - The Battle.net friend's index on the friends list

==Patch changes==
* {{Patch 6.2.4|note=Replaced <code>presenceID</code> with <code>bnetIDAccount</code>.}}
```