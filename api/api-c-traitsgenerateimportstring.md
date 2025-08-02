# API C Traits.GenerateImportString

**Contributor:** Kemayo

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Traits|system=SharedTraits}}
Generate a talent loadout string for a given loadout
 importString = C_Traits.GenerateImportString(configID)

==Arguments==
:;configID:{{apitype|number}} a talent loadout, e.g. from {{api|C_ClassTalents.GetConfigIDsBySpecID}} or simply {{api|C_ClassTalents.GetActiveConfigID}}.

==Returns==
:;importString:{{apitype|string}} a talent loadout string, which can be used to import the loadout, can be sent to a friend, or used on external websites. An empty string is returned if the client can't find data for the loadout.

==Details==
No data is available until the first {{api|t=e|TRAIT_CONFIG_LIST_UPDATED}}. When reloading UI, data is available immediately.

This API works only for talent loadouts for the current character, but it does work for other specs. The returned string, can be used in the Talent Tree UI to import the loadout, and its format has been documented by Blizzard in [https://github.com/Gethe/wow-ui-source/blob/live/Interface/AddOns/Blizzard_PlayerSpells/ClassTalents/Blizzard_ClassTalentImportExport.lua Blizzard_ClassTalentImportExport.lua].

It's important to note, that if you use this API with a loadout outside your current spec, the Specialization ID in the header will be incorrect, since that will always reflect your current spec instead. So you may want to change the header with code like this:
<syntaxhighlight lang="lua">
-- note: this example is made for Serialization Version 1 specifically, and if blizzard updates the format, this may no longer work
local bitWidthHeaderVersion = 8;
local bitWidthHeaderSpecID = 16;
local function fixLoadoutString(loadoutString, specID)
   local exportStream = ExportUtil.MakeExportDataStream();
   local importStream = ExportUtil.MakeImportDataStream(loadoutString);
   
   if importStream:ExtractValue(bitWidthHeaderVersion) ~= 1 then
      return nil; -- only version 1 is supported
   end
   
   local headerSpecID = importStream:ExtractValue(bitWidthHeaderSpecID);
   if headerSpecID == specID then
      return loadoutString; -- no update needed
   end
   
   exportStream:AddValue(bitWidthHeaderVersion, 1);
   exportStream:AddValue(bitWidthHeaderSpecID, specID);
   local remainingBits = importStream:GetNumberOfBits() - bitWidthHeaderVersion - bitWidthHeaderSpecID;
   -- copy the remaining bits in batches of 16
   while remainingBits > 0 do
      local bitsToCopy = math.min(remainingBits, 16);
      exportStream:AddValue(bitsToCopy, importStream:ExtractValue(bitsToCopy));
      remainingBits = remainingBits - bitsToCopy;
   end
   
   return exportStream:GetExportString();
end

local spec = 62; -- assuming you're playing mage
local configID = C_ClassTalents.GetConfigIDsBySpecID(specID)[1]; -- assuming you have an arcane loadout
print(fixLoadoutString(C_Traits.GenerateImportString(configID), specID))
</syntaxhighlight>


{{apinavbox|C_Traits}}
```