# API C ChatInfo.RegisterAddonMessagePrefix

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ChatInfo|system=ChatInfo}}
Registers an addon message prefix to receive messages for that prefix.
 result = C_ChatInfo.RegisterAddonMessagePrefix(prefix)

==Arguments==
:;prefix:{{apitype|string}} - The message prefix to register for delivery, at most 16 characters.

==Returns==
:;result:{{apitype|Enum.RegisterAddonMessagePrefixResult}} - Result code indicating if the prefix was registered successfully.
{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
! Value !! Field !! Description
|-
| 0 || {{apiname|Success}} || 
|-
| 1 || {{apiname|DuplicatePrefix}} || 
|-
| 2 || {{apiname|InvalidPrefix}} || 
|-
| 3 || {{apiname|MaxPrefixes}} || 
|}

==Details==
* Registering prefixes does not persist after doing a /reload.
* It's recommended to use the addon name as a prefix (provided it fits within the 16 byte limit) since it's more likely to be unique and other addon authors will have an easier time instead of figuring out what addon a certain abbreviation belongs to. See the [https://www.townlong-yak.com/globe/wut/#q:C_ChatInfo.RegisterAddonMessagePrefix Globe wut] page for a list of addons that use this API to avoid collisions.

==Patch changes==
====<font color="#4ec9b0">Retail</font>====
* {{Patch 10.2.7|note=Now returns a result code, rather than a boolean.</code>}}
* {{Patch 8.0.1|note=Moved to <code>C_ChatInfo.RegisterAddonMessagePrefix()</code>}}
* {{Patch 4.1.0|note=Added as <code>RegisterAddonMessagePrefix()</code>}}

====<font color="#4ec9b0">Classic</font>====
* {{Patch 4.4.0|note=Now returns a result code, rather than a boolean.</code>}}

==See also==
* {{api|C_ChatInfo.GetRegisteredAddonMessagePrefixes}}()
* {{api|C_ChatInfo.IsAddonMessagePrefixRegistered}}()
* {{api|C_ChatInfo.SendAddonMessage}}()
```