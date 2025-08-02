# API IsRecognizedName

**Contributor:** Meorawr

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if a given character name is recognized by the client.
 isRecognized = IsRecognizedName(text, includeBitfield, excludeBitfield)

==Arguments==
:;text:{{apitype|string}} - Name of the character to test.
:;includeBitfield:{{apitype|number}} - Bitfield of filters that the name must match at least one of.
:;excludeBitfield:{{apitype|number}} - Bitfield of filters that the name must not match any of.

==Returns==
:;isRecognized:{{apitype|boolean}} - <code>true</code> if the character name is recognized by the client and passes the requested filters.

==Filters==
The filters used by this function are the same as the autocompletion flags used by {{api|GetAutoCompleteResults}}().
{{:AutocompleteFlag}}

==Details==

* This function may return false for some filters if the player enters, exits, and re-enters the local area of interest of the tested character name.
* When testing character names that are on the same Battle.net account, the character name must not include any realm identifier if the currently logged in character is on the same realm.

==See also==
* {{api|GetAutoCompleteResults}}()
```