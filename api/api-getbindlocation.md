# API GetBindLocation

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the subzone the character's Hearthstone is set to.
 location = GetBindLocation()

==Returns==
Returns the String name of the subzone the player's Hearthstone is set to, e.g. "Tarren Mill", "Crossroads", or "Brill".

==Example==
 bindLocation = GetBindLocation();

If the player's Hearthstone is set to the inn at Allerian Stronghold then bindLocation assigned "Allerian Stronghold".
```