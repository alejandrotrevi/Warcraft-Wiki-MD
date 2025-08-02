# API GetShapeshiftForm

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the zero-based index of current form/stance.
 index = GetShapeshiftForm([flag])

==Arguments==
:;flag:{{apitype|boolean?}} - True if return value is to be compared to a macro's conditional statement. This makes it always return zero for Presences and Auras. False or nil returns an index based on which button to highlight on the shapeshift/stance bar left to right starting at 1.

==Returns==
:;index:{{apitype|number}} - one of the following:

{| class="darktable" style="margin-left: 2em"
|
:;All classes:
:: &nbsp; 0. humanoid form

:;{{text|druid|Druid}}:
:# Bear Form
:# Cat Form
:# Travel Form / Aquatic Form / Flight Form (all 3 location-dependent versions of Travel Form count as Form 3)
:# The first known of: Moonkin Form, Treant Form, Stag Form (in order)
:# The second known of: Moonkin Form, Treant Form, Stag Form (in order)
:# The third known of: Moonkin Form, Treant Form, Stag Form (in order)
:::Note: The last 3 are ordered.  For example, if you know Stag Form only, it is form 4.  If you know both Treant and Stag, Treant is 4 and Stag is 5.  If you know all 3, Moonkin is 4, Treant 5, and Stag 6.

:;{{text|priest|Priest}}:
:# Shadowform

:;{{text|rogue|Rogue}}:
:# Stealth
:# Vanish / Shadow Dance (for Subtlety rogues, both Vanish and Shadow Dance return as Form 1)

:;{{text|shaman|Shaman}}:
:# Ghost Wolf

:;{{text|warrior|Warrior {{Wow-inline}}}}:
:# Battle Stance
:# Defensive Stance
:# Beserker Stance

:;{{text|hunter|Hunter {{Wow-inline}}}}:
:# Aspect of the Hawk
|}

==Details==
* For some classes the return value is nil during the loading process. You need to wait until UPDATE_SHAPESHIFT_FORMS fires to get correct return values.
```