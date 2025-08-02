# API ProcessExceptionClient

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|protected|note=This function will silently do nothing if called from an insecure execution path.}}
Generates textual error logs for any current Lua error.
 ProcessExceptionClient(description)

==Arguments==
:;description:{{apitype|string}} - The description of the error being processed.

==Details==
* This function is invoked by the default global error handler to trigger the generation of textual error logs when a Lua error occurs in a secure execution path.
* The {{api|t=c|luaErrorExceptions}} console variable must be enabled for this function to have any effect.

==Patch changes==
* {{Patch 10.0.0|note=Added <code>description</code> parameter.}}
* {{Patch 9.0.1|note=Added.}}
```