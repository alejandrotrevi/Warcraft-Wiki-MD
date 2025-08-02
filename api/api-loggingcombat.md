# API LoggingCombat

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Gets or sets whether logging combat to Logs\WoWCombatLog.txt is enabled.
 isLogging = LoggingCombat([newState])

==Arguments==
:;newState:{{apitype|boolean?}} - If passed, enables/disables combat logging. If not passed, queries the current state without changing it.
:::To query the current state, LoggingCombat() must be called with zero arguments. One should not pass nil explicitly, since the behavior is the same as passing false (it disables combat logging).

==Returns==
:;isLogging:{{apitype|boolean?}} - Whether combat logging is now enabled/disabled.
:::true: Combat logging is enabled
:::false: Combat logging is disabled
:::nil: The function call was rate limited. The combat logging state was not changed, and it is unknown whether combat logging is currently enabled or disabled.

==Details==
: This function is heavily rate limited, even when only querying the state. The limit is 5 calls per 10 seconds, shared across all addons (and the /combatlog command). Subsequent calls will return nil, and will not change the combat logging state.

==Example==
Enable combat logging:
 /run local x=LoggingCombat(true)UIErrorsFrame:AddMessage(x and"Combat logging is now enabled." or "Failed to enable combat logging, try again in 10 seconds.",1,0,0)

Disable combat logging:
 /run local x=LoggingCombat(false)UIErrorsFrame:AddMessage(x==false and"Combat logging is now disabled."or"Failed to disable combat logging, try again in 10 seconds.",1,0,0)

Query combat logging state:
 /run local x=LoggingCombat()UIErrorsFrame:AddMessage(x==nil and"Failed to query combat logging state, try again in 10 seconds."or"Combat logging is currently "..(x and"enabled."or"disabled."),1,0,0)
```