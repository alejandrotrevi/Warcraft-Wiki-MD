# API GetFunctionCPUUsage

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about CPU usage by a function.
 usage, calls = GetFunctionCPUUsage(func, includeSubroutines)

==Arguments==
:;func:{{apitype|function}}
:;includeSubroutines:{{apitype|boolean}}

==Returns==
:;usage:{{apitype|number}}
:;calls:{{apitype|number}}

==Details==
* Only returns valid data if the {{api|t=c|scriptProfile}} CVar is set to 1; returns 0 otherwise.
```