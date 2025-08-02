# API C TTSSettings.GetVoiceOptionID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_TTSSettings|system=TTSSettings}}
Get the user's preferred text to speech voices.
 voiceID = C_TTSSettings.GetVoiceOptionID(voiceType)

==Arguments==
:;voiceType:{{apitype|Enum.TtsVoiceType}}
{{:Enum.TtsVoiceType|nocaption=1}}

==Returns==
:;voiceID:{{apitype|number}} - Used with {{api|C_VoiceChat.SpeakText}}().

==Patch changes==
* {{Patch 9.1.5|note=Added.}}

{{apinavbox|C_VoiceChat_TextToSpeech}}
```