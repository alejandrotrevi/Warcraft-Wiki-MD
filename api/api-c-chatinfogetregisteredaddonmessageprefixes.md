# API C ChatInfo.GetRegisteredAddonMessagePrefixes

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ChatInfo|system=ChatInfo}}
Returns addon message prefixes the client is currently registered to receive.
 registeredPrefixes = C_ChatInfo.GetRegisteredAddonMessagePrefixes()

==Returns==
:;registeredPrefixes:{{apitype|string[]}}

==Patch changes==
* {{Patch 8.0.1|note=Moved to <code>C_ChatInfo.GetRegisteredAddonMessagePrefixes()</code>}}
* {{Patch 4.1.0|note=Added as <code>GetRegisteredAddonMessagePrefixes()</code>}}

==See also==
* {{api|C_ChatInfo.IsAddonMessagePrefixRegistered}}()
* {{api|C ChatInfo.RegisterAddonMessagePrefix}}()
```