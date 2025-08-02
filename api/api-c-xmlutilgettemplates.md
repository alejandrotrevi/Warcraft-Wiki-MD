# API C XMLUtil.GetTemplates

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns a list of all registered XML templates.
 templates = C_XMLUtil.GetTemplates()

==Returns==
:;templates:{{apitype|XMLTemplateListInfo[]}} - An array of tables for each registered XML template.

{{:Struct_XMLTemplateListInfo|nocaption=1}}

==Example==
The following snippet will print all the names and frame types of registered XML templates.
<syntaxhighlight lang="lua">
for _, template in ipairs(C_XMLUtil.GetTemplates()) do
    print(template.name, template.type)
end
</syntaxhighlight>

==Patch changes==
* {{Patch 10.0.0|note=Added.}}
```