# API GetNumSockets

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the number of sockets for an item in the socketing window.
 numSockets = GetNumSockets()

==Returns==
:;numSockets:{{apitype|number}} - The number of sockets in the item currently in the item socketing window. If the item socketing window is closed, 0.

==Example==
<syntaxhighlight lang="lua">
for i = 1, GetNumSockets() do
    print(GetSocketInfo(i))
end
</syntaxhighlight>

==Details==
This function is only useful if the item socketing window is currently visible.
```