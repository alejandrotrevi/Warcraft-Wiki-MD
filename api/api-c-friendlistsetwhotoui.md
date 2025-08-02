# API C FriendList.SetWhoToUi

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Sets how the result of a [[MACRO who|/who]] request will be delivered.

 C_FriendList.SetWhoToUi(whoToUi)

==Arguments==
:;whoToUi:{{apitype|boolean|default=false}} - If <code>true</code> the results will always be delivered as a {{api|t=e|WHO_LIST_UPDATE}} event and displayed in the '''FriendsFrame'''. If <code>false</code> the results may be returned as a sequence of {{api|t=e|CHAT_MSG_SYSTEM}} events (up to 3 results) ''or'' a WHO_LIST_UPDATE event (4+ results).

==Details==
* The /who query is subject to a server-side throttle; throttled requests are silently dropped.
* This setting does not persist between relog/reload.
* The <code>FriendsFrame</code> will automatically display open to display the results when the WHO_LIST_UPDATE event is triggered. You may hide the frame using <code>HideUIPanel(FriendsFrame)</code> (protected during combat lockdown), or temporarily unregister it from WHO_LIST_UPDATE to prevent this behavior if your addon relies on performing /who queries in the background.

==Patch changes==
* {{Patch 8.1.0|note=Moved to <code>C_FriendList.SetWhoToUi()</code> ⚠️ ''Note the lowercase <code>i</code> at the end.''}}
* {{Patch 1.0.0|note=Added as <code>SetWhoToUI()</code>}}
```