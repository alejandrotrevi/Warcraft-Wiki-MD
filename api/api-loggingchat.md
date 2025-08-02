# API LoggingChat

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Gets or sets whether logging chat to Logs\WoWChatLog.txt is enabled.
 isLogging = LoggingChat([newState])

==Arguments==
:;newState:{{apitype|boolean?}} - toggles chat logging

==Returns==
:;isLogging:{{apitype|boolean?}} - current state of logging

==Example==
 if (LoggingChat()) then
   print("Chat is already being logged")
 else
   print("Chat is not being logged - starting it!")  
   LoggingChat(1)
   print("Chat is now being logged to Logs\\WOWChatLog.txt")
 end
```