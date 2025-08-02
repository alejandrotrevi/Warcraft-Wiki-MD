# API BNGetFOFInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for the specified friend of a Battle.net friend.
 friendID, accountName, isMutual = BNGetFOFInfo(mutual, nonMutual, index)

==Arguments==
:;mutual:{{apitype|boolean}} - Should the list include mutual friends (I.e. people who you and the person referenced by presenceID are both friends with).
:;nonMutual:{{apitype|boolean}} - Should the list include non-mutual friends.
:;index:{{apitype|number}} - The index of the entry in the list to retrieve (1 to BNGetNumFOF(...))

==Returns==
:;friendID:{{apitype|number}} - a unique numeric identifier for this friend for this session
:;accountName:{{apitype|string}} - a [[Kstring]] representing the friend's name (As of 4.0)
:;isMutual:{{apitype|boolean}} - true if this person is a direct friend of yours, false otherwise.
```