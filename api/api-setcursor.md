# API SetCursor

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Sets the current cursor texture.
 changed = SetCursor(cursor)

==Arguments==
:;cursor:{{apitype|string,nil}} - cursor to switch to; either a built-in cursor identifier (like "ATTACK_CURSOR"), path to a cursor texture (e.g. "Interface/Cursor/Taxi"), or explicitly <code>nil</code> to reset to a default cursor.

==Returns==
:;changed:{{apitype|boolean?}} - Seems to return false when the given <code>cursor</code> string argument was different from the previous one, otherwise returns true.

==Details==
* If the cursor is hovering over WorldFrame, the SetCursor function will have no effect - cursor is locked to reflect what the player is currently pointing at.
* Texture paths may be suffixed by ".crosshair" to offset the position of the texture such that it will be centered on the cursor.
* If called with an invalid argument, the cursor is replaced by a black square.

==Patch changes==
* {{Patch 3.1.0|note=Now always returns <code>1</code>.}}
* {{Patch 1.11.0|note=Now accepts a <code>nil</code> argument to reset to default cursor.}}
```