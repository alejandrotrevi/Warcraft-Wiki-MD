# API C FriendList.GetNumWhoResults

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Get the number of entries resulting from your most recent /who query.

 numWhos, totalNumWhos = C_FriendList.GetNumWhoResults()

==Returns==
:;numWhos:{{apitype|number}} - Number of results returned
:;totalNumWhos:{{apitype|number}} - Number of results to display

==Details==
* Both return values never seem to go over 50.
* If <code>totalNumWhos</code> would be bigger than 50, the amount shown will be capped to <code>MAX_WHOS_FROM_SERVER</code> (50) in FrameXML.<sup>[https://github.com/Gethe/wow-ui-source/blob/8cc5f29bcd45dcbe3ed293cfb146b0178b2d4e92/Interface/FrameXML/FriendsFrame.lua#L791]</sup>
```