# API SecureCmdOptionParse

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Evaluates macro conditionals without the need of a macro.
 result, target = SecureCmdOptionParse(options)

==Arguments==
:;options:{{apitype|string}} - a [[secure command options]] string to be parsed, e.g. "[mod:alt] ALT is held down; [mod:ctrl] CTRL is held down, but ALT is not; neither ALT nor CTRL is held down".

==Returns==
:;result:{{apitype|string}} - value of the first satisfied clause in ''options'', or no return (nil) if none of the conditions in ''options'' are satisfied.
:;target:{{apitype|string}} - the target of the first satisfied clause in ''options'' (using either the <code>target=...</code> or <code>@...</code> conditional), nil if the clause does not explicitly specify a target, or no return (nil) if none of the conditions in ''options'' are satisfied.

==Details==
* Note that item links cannot be part of options string as they contain square brackets [], which get interpreted by the parser as conditions.
* This function is available in the [[RestrictedEnvironment]], and is used to evaluate the options for secure [[macro commands]].

==See also==
* [[Secure command options]]
* [[SecureStateDriver]]
```