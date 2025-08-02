# API LocalizedClassList

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Localization}}
Returns a table with localized class names.
 result = LocalizedClassList([isFemale])

==Arguments==
:;isFemale:{{apitype|boolean?|default=false}}

==Returns==
:;result:{{apitype|table}}

==Example==
Dumps the result table (enUS locale).
<syntaxhighlight lang="lua">
/dump LocalizedClassList()

[1]={
    Adventurer="Adventurer"
    DEATHKNIGHT="Death Knight",
    DEMONHUNTER="Demon Hunter",
    DRUID="Druid",
    EVOKER="Evoker",
    HUNTER="Hunter",
    MAGE="Mage",
    MONK="Monk",
    PALADIN="Paladin",
    PRIEST="Priest",
    ROGUE="Rogue",
    SHAMAN="Shaman",
    WARLOCK="Warlock",
    WARRIOR="Warrior",
}
</syntaxhighlight>
```