# API C ClassTalents.InitializeViewLoadout

**Contributor:** Numynum

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ClassTalents|system=ClassTalents}}
Prepares the <code>Constants.TraitConsts.VIEW_TRAIT_CONFIG_ID</code> configID, with spec and level information.
 C_ClassTalents.InitializeViewLoadout(specID, level)

==Arguments==
:;specID:{{apitype|number}} - [[SpecializationID]] e.g. <code>PlayerUtil.GetCurrentSpecID()</code>
:;level:{{apitype|number}}

==Details==
This API, is used by Blizzard, to power their inspect UI, when clicking on a talent link ingame. Using this API yourself, can disrupt that usage, so if you're using this API to build some kind of cache, it's encouraged to do this during initial loading.

Can be used in conjunction with {{api|C_ClassTalents.ViewLoadout}} to build a cache of talent information, useful if you want to for example create an addon with some kind of talent picker. [https://github.com/NumyAddon/LibTalentTree-1.0 LibTalentTree-1.0] provides enriched information, based on this API.

For example, to create a list of talent spellIDs for a given spec, you can run the following code:
<syntaxhighlight lang="lua">
function GetSpellIDListBySpecID(specID)
    C_ClassTalents.InitializeViewLoadout(specID, 10) -- the level doesn't really matter for this usage
    C_ClassTalents.ViewLoadout({}) -- it's required to call ViewLoadout, even if it's with an empty table, as the API will not work as expected otherwise

    local list = {}

    local configID = Constants.TraitConsts.VIEW_TRAIT_CONFIG_ID

    local configInfo = C_Traits.GetConfigInfo(configID)
    if configInfo == nil then return end

    for _, treeID in ipairs(configInfo.treeIDs) do -- in the context of talent trees, there is only 1 treeID
        local nodes = C_Traits.GetTreeNodes(treeID)
        for i, nodeID in ipairs(nodes) do
            local nodeInfo = C_Traits.GetNodeInfo(configID, nodeID)
            for _, entryID in ipairs(nodeInfo.entryIDs) do -- each node can have multiple entries (e.g. choice nodes have 2)
                local entryInfo = C_Traits.GetEntryInfo(configID, entryID)
                if entryInfo and entryInfo.definitionID then
                    local definitionInfo = C_Traits.GetDefinitionInfo(entryInfo.definitionID)
                    if definitionInfo.spellID then
                        table.insert(list, definitionInfo.spellID)
                    end
                end
            end
        end
    end
    return list
end
</syntaxhighlight>

{{apinavbox|C_Traits}}
```