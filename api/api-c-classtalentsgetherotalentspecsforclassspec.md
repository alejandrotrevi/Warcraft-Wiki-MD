# API C ClassTalents.GetHeroTalentSpecsForClassSpec

**Contributor:** Numynum

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ClassTalents|system=ClassTalents}}
Returns the SubTreeIDs of the Hero Talent Specializations available to a Class Specialization and config; Returns nothing if none available
 subTreeIDs, requiredPlayerLevel = C_ClassTalents.GetHeroTalentSpecsForClassSpec([configID [, classSpecID]])

==Arguments==
:;configID:{{apitype|number?}} - If not supplied, defaults to the player's active config
:;classSpecID:{{apitype|number?}} - [[SpecializationID]] e.g. <code>PlayerUtil.GetCurrentSpecID()</code>, defaults to current spec

==Returns==
:;subTreeIDs:{{apitype|number[]?}} - SubTreeIDs of each Hero Talent Specialization
:;requiredPlayerLevel:{{apitype|number?}} - The player level at which one of the Hero Talent Specializations can be activated

==Values==
:<span class="noexcerpt" data-nosnippet>''Linked from: [[HeroSpecID]]''</span>
{{:HeroSpecID}}

==Details==
Does not return any information when logging in initially. On reloads, the information ''is'' available right away.
Besides the <code>requiredPlayerLevel</code>, all information can be gathered by iterating through NodeInfo and EntryInfo instead.

{{apinavbox|C_Traits}}
```