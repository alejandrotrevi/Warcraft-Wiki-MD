# API RunBinding

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Executes a key binding.
 RunBinding(command [, up])

==Arguments==
:;command:{{apitype|string}} - Name of the key binding to be executed
:;up:{{apitype|string?}} - If "up", the binding is run as if the key was released.

==Example==
The call below toggles the display of the FPS counter, as if CTRL+R was pressed.
 RunBinding("TOGGLEFPS");

==Details==
The "command" argument must match one of the (usually capitalized) binding names in a Bindings.xml file. This can be a name that appears in the Blizzard FrameXML Bindings.xml, or one that is specified in an AddOn.

RunBinding cannot be used to call a [[:Category:World of Warcraft API/Protected Functions|Protected Function]] from insecure execution paths.

By default, the key binding is executed as if the key was pressed down, in other words the keystate variable will have value "down" during the binding's execution. By specifying the optional second argument (the actual string "up"), the binding is instead executed as if the key was released, in other words the keystate variable will have value "up" during the binding's execution.
```