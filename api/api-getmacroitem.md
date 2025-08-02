# API GetMacroItem

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about the item a given macro is set to use.
 itemName, itemLink = GetMacroItem(name)

==Arguments==
:;name:{{apitype|number,string}} - The macro index to query, or the name of the macro to query.

==Returns==
:;itemName:{{apitype|string}} - The localized name of the item.
:;itemLink:{{apitype|string}} : [[ItemLink]] - The localized link of the item.

==Example==
<syntaxhighlight lang="lua">
local macroName = "MyMacro"
local index = GetMacroIndexByName(macroName)
if index then 
    local itemId, itemLink = GetMacroItem(index)
    if itemId then
        print("Item to use inside macro", itemId, itemLink)
    end
end
</syntaxhighlight>
```