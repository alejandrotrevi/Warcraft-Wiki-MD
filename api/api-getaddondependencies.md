# API GetAddOnDependencies

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.0|removed=11.0.2}}
Returns the TOC dependencies of an addon.
 dep1, dep2, ... = GetAddOnDependencies(name)

==Arguments==
{{:AddOnInfo}}

==Returns==
:;dep1, dep2, ...:{{apitype|string}} - List of addon names that are a required dependency.
{{apinavbox|AddOn}}
```