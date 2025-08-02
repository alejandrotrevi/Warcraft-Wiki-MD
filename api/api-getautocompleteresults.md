# API GetAutoCompleteResults

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns possible player names matching a given prefix string and specified requirements.
 results = GetAutoCompleteResults(text, numResults, cursorPosition, allowFullMatch, includeBitField, excludeBitField)

==Arguments==
:;text:{{apitype|string}} - First characters of the possible names to be autocompleted
:;numResults:{{apitype|number}} - Number of results desired.
:;cursorPosition:{{apitype|number}} - Position of the cursor within the editbox (i.e. how much of the text string should be matching).
:;allowFullMatch:{{apitype|boolean}}
:;includeBitField:{{apitype|number}} - Bit mask of [[#Filter values|filters]] that the results '''must''' match at least one of.
:;excludeBitField:{{apitype|number}} - Bit mask of [[#Filter values|filters]] that the results '''must not''' match any of.

===Filter values===
The <code>includeBitField</code> and <code>excludeBitField</code> bit mask parameters can be composed from the following components:
{{:AutocompleteFlag}}

==Returns==
:;results:{{apitype|table[]}} - Auto-completed names of players that satisfy the requirements.
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| bnetID || {{apitype|number}} ||
|-
| name || {{apitype|string}} || The realm part can possibly be omitted for players on the same realm.<br>This format might be inconsistent (on Classic), e.g. <code>Foo-Nethergarde Keep</code> and <code>Foo-MirageRaceway</code>
|-
| priority || {{apitype|number}} || 
|}
<!-- ood
==Example==
Assuming you are sending a mail to someone whose name starts with "a", and that the Send Mail window is open
 GetAutoCompleteResults("a",
                        SendMailNameEditBox.autoCompleteParams.include,
                        SendMailNameEditBox.autoCompleteParams.exclude,
                        AUTOCOMPLETE_MAX_BUTTONS+1,
                        SendMailNameEditBox:GetCursorPosition())
-->

==Patch changes==
* {{Patch 3.2.0|note=Added.}}
```