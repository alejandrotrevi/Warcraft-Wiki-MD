# API GetLatestThreeSenders

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns up to three senders of unread mail.
 sender1, sender2, sender3 = GetLatestThreeSenders()

==Returns==
:;sender1:{{apitype|string?}} - Name of the sender ("Bob", "Alliance Auction House", ...), or nil if unavailable.
:;sender2:{{apitype|string?}}
:;sender3:{{apitype|string?}}
```