---
order: 123
pcx-content-type: reference
---

# Firewall fields

The Firewall fields contain rules to block requests that contain specific types of content.

## FirewallMatchesActions

<TableWrap>

| Value | Action | Description |
|---|---|---|
| `unknown` | Unknown | Take no other action. |
| `allow` | Allow | Bypass all subsequent rules. |
| `block` | Drop | Block with an HTTP 403 response. |
| `challenge` | Challenge Drop | Issue a CAPTCHA challenge. |
| `jschallenge` | Challenge Drop | Issue a JS challenge. |
| `log` | Log | Take no action other than logging the event. |
| `connectionClose` | Close | Close connection. |
| `challengeSolved` | Allow | Allow once CAPTCHA challenge solved. |
| `challengeFailed` | Drop | Block following invalid CAPTCHA solve attempt. |
| `challengeBypassed` | Allow | CAPTCHA challenge not issued because visitor had previously passed a CAPTCHA challenge.|
| `jschallengeSolved` | Allow | Allow once JS challenge solved. |
| `jschallengeFailed` | Drop | Drop if JS challenge failed. |
| `jschallengeBypassed` | Allow | JS challenge not issued because the visitor had previously passed a JS or CAPTCHA challenge.  |
| `bypass` | Allow | Bypass all subsequent firewall rules. |
| `managedChallenge` | Challenge Drop | Issue managed challenge. |
| `managedChallengeSkipped` | Allow | Skip managed challenge and allow. |
| `managedChallengeNonInteractiveSolved` | Allow | Allow once the managed challenge is solved via non-interactive interstitial page. |
| `managedChallengeInteractiveSolved` | Allow | Allow once the managed challenged is solved via interactive interstitial page. |
| `managedChallengeBypassed` | Allow | Challenge was not presented because visitor had clearance from previous challenge. |

</TableWrap>

## FirewallMatchesSources

<TableWrap>

| Value | Description |
|---|---|
| `unknown` | Used if an event is received from a new source but the logging system has not been updated. |
| `asn` | Allow or block based on autonomous system number. |
| `country` | Allow or block based on country. |
| `ip` | Allow or block based on IP address. |
| `ipRange` | Allow or block based on range of IP addresses. |
| `securityLevel` | Allow or block based on requester's security level. |
| `zoneLockdown` | Restrict all access to a specific zone. |
| `waf` | Allow or block based on the WAF product settings. This is the WAF/managed rules system that is being phased out. |
| `firewallRules` | Allow or block based on a zone's firewall rules configuration. |
| `uaBlock` | Allow or block based on the Cloudflare User Agent Blocking product settings. |
| `rateLimit` | Allow or block based on a rate limiting rule, whether set by you or by Cloudflare. |
| `bic` | Allow or block based on the Browser Integrity Check product settings. |
| `hot` | Allow or block based on the Hotlink Protection product settings. |
| `l7ddos` | Allow or block based on the L7 DDoS product settings. |
| `validation` | Allow or block based on a request that is invalid (cannot be customized.) |
| `botFight` | Allow or block based on the Bot Fight Mode (classic) product settings. |
| `botManagement` | Allow or block based on the Bot Management product settings. |
| `dlp` | Allow or block based on the Data Loss Prevention product settings. |
| `firewallManaged` | Allow or block based on the Firewall Managed Rules product settings. |
| `firewallCustom` | Allow or block based on a rule configured in the Firewall Custom Rulesets. |

</TableWrap>
