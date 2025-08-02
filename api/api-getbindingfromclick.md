# API GetBindingFromClick

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Gets the binding action from a key or button press.

 command = GetBindingFromClick(keyOrButton)

==Arguments==

:;keyOrButton:{{apitype|string}} - The mouse button or key that was pressed.

==Returns==

:;command:{{apitype|string}} - The command that keyOrButton is bound to. This is the same type that is passed to [[RunBinding]].
```