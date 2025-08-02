# API C Scenario.GetProvingGroundsInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for the current [[Proving Grounds]] trial.
 difficulty, curWave, maxWave, duration = C_Scenario.GetProvingGroundsInfo()

==Returns==
:;difficulty:{{apitype|number}} - difficulty ID of the current trial, 1 for bronze.
:;curWave:{{apitype|number}} - current wave index, ascending from 1.
:;maxWave:{{apitype|number}} - number of waves in the trial.
:;duration:{{apitype|number}} - total amount of time allotted to complete the current wave; 0 if the wave is not time-limited.

==Details==
* If no [[Proving Grounds]] trial is currently active, all four return values are 0.
* The duration represents the total amount of time allotted to complete the current wave, and does not change. The actual counting-down timer is available through {{api|GetWorldElapsedTime}}.

==Patch changes==
* {{Patch 5.4.0|note=Added.}}
```