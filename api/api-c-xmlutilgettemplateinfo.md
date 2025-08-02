# API C XMLUtil.GetTemplateInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about a defined XML template.
 info = C_XMLUtil.GetTemplateInfo(name)

==Arguments==
:;name:{{apitype|string}} - The name of the template to query.

==Returns==
:;info:{{apitype|XMLTemplateInfo?}} - Information about the queried template if found, or nil if the template does not exist.

{{:Struct_XMLTemplateInfo|nocaption=1}}

==Patch changes==
* {{Patch 10.0.0|note=Added.}}
```