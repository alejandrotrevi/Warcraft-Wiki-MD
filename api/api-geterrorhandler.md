# API geterrorhandler

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the currently set error handler.
 handler = geterrorhandler()

==Returns==
:;handler:{{apitype|function}} - The current error handler. Receives a message as an argument, normally a string that is the second return value from {{api|pcall}}().

==Example==
<syntaxhighlight lang="lua">
local myError = "Something went horribly wrong!"
geterrorhandler()(myError)
</syntaxhighlight>
```