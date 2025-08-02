# API RunMacro

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|protected|note=Use the "macro" action type of [[SecureActionButtonTemplate]].}}
Executes a macro.
 RunMacro(name)

==Arguments==
:;name:{{apitype|number,string}} - the position or name of the macro. Starting at the top left macro with 1, counting from left to right and top to bottom. The IDs of the first page (all characters) range from 1-36, the second page 37-54.

==Patch changes==
* {{Patch 2.0.1|note=Protected.}}
```