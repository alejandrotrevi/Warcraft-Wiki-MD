# API GetMacroBody

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the body (macro text) of a macro.
 body = GetMacroBody(macro)

==Arguments==
:;macro:{{apitype|number,string}} - Macro index or name.

==Returns==
:;body:{{apitype|string?}} - The macro body or nothing if the macro doesn't exsist.

==Example==
 /dump GetMacroBody("Flash Heal")
<syntaxhighlight lang="lua">
[1]="#showtooltip\
/cast [@target,help,nodead][@player] Flash Heal\
"
</syntaxhighlight>
```