# World of Warcraft AddOns

An index of the WoW addons I maintain. Each one lives in its own repository —
this is just the front door.

| AddOn | What it does | Client | Licence | Repository |
| --- | --- | --- | --- | --- |
| **Eloquence** | Linguistic chat filters and racial dialects for roleplay | 12.1 | MIT | [Zethrel/Eloquence](https://github.com/Zethrel/Eloquence) |
| **Enemy RP** | Carries roleplay profiles and chat across the faction divide | 12.0.7 | GPL-3.0 | [Zethrel/Enemy-RP](https://github.com/Zethrel/Enemy-RP) |
| **Exposition** | Writes long roleplay posts and sends them to chat without breaking words | 12.1 | All rights reserved | [Zethrel/exposition](https://github.com/Zethrel/exposition) |
| **KillThemAll** | Randomly plays Old Gods whispers, like the sha-touched weapons of MoP | 12.0.7 · Classic | MIT | [Zethrel/kill-them-all-addon](https://github.com/Zethrel/kill-them-all-addon) |
| **Roleplay Event Helper** | Announces your event's house rules and adjudicates `/roll` results | 12.1 | All rights reserved | [Zethrel/Roleplay-event-helper](https://github.com/Zethrel/Roleplay-event-helper) |
| **SayWhat** | Tracks who talks in /say range and mirrors them into a Nearby window | 12.1 | All rights reserved | [Zethrel/say-what](https://github.com/Zethrel/say-what) |

Five of the six are roleplay addons, which is not an accident — that is what I
play. KillThemAll is the odd one out, and it is a rescue rather than a
creation.

---

## Eloquence

A revival of the classic roleplaying chat addon, rebuilt for modern retail. It
gives every speaker an accent or dialect based on their race, and layers
linguistic filters over the chat you read — correcting spelling, expanding
acronyms, censoring profanity, and dragging modern turns of phrase into
something that sounds like it belongs in Azeroth.

Written from scratch. MIT licensed.

→ [Repository](https://github.com/Zethrel/Eloquence) ·
[Releases](https://github.com/Zethrel/Eloquence/releases) ·
[CurseForge](https://www.curseforge.com/wow/addons/eloquence-revived)

## Enemy RP

The game will not deliver an addon message from a Horde character to an
Alliance one, so Total RP 3, MyRolePlay and XRP all fall silent the moment the
other faction walks into the tavern. Enemy RP carries the same profile data
over the channels that *do* cross factions — party, guild, Battle.net friends,
or a shared community — and hands what arrives to whichever roleplay addon you
already run. It speaks Mary Sue Protocol, the format all three share, so a
Horde Total RP user and an Alliance XRP user can read each other with nothing
configured on either side. Say, emote and yell are relayed too, so you can hold
a conversation rather than just read a profile.

Early days: the protocol is implemented and tested end to end against a
simulated client, but it has not yet met a live crowd. Cross RP proved this was
possible and Enemy RP owes it the idea, but none of its code — it is written
against the public interfaces, and GPL-3.0 so it cannot quietly become closed
the way its predecessor did.

→ [Repository](https://github.com/Zethrel/Enemy-RP) ·
[Releases](https://github.com/Zethrel/Enemy-RP/releases)

## Exposition

Chat cuts you off at 255 characters. Splitting a long post by hand leaves you
counting characters; splitting it naively leaves you with a sentence torn
across two lines mid-word. Exposition takes the whole post in one window,
previews exactly what will be sent message by message, and never breaks a word
— if a word does not fit, it leads the next message instead. Pick a channel, a
marker style and a delay, press send, and the rest follow on a timer you can
stop at any point.

→ [Repository](https://github.com/Zethrel/exposition) ·
[Releases](https://github.com/Zethrel/exposition/releases)

## KillThemAll

Randomly plays Old Gods whispers audio files, reproducing the effect of the
sha-touched weapons of Mists of Pandaria. Y'Shaarj, C'Thun, Yogg-Saron and
Il'Gynoth are all available, with a configurable delay and sound channel.

Originally by [Thex](https://github.com/Thex-PiedDroit/KillThemAll)
([CurseForge](https://www.curseforge.com/wow/addons/killthemall)), which stopped
at Interface 100207 (Dragonflight 10.2.7). This fork updates it for Midnight —
bumping the `.toc` alone was not enough, because three globals the addon calls
were removed from retail in 11.0. Classic and Classic Era builds ship alongside
the retail one. MIT licensed, as upstream.

→ [Repository](https://github.com/Zethrel/kill-them-all-addon) ·
[Releases](https://github.com/Zethrel/kill-them-all-addon/releases)

## Roleplay Event Helper

For people who host roleplay events. Build a preset of your house rules —
health per armor class, what a `/roll` has to hit to succeed, turn order,
whatever else you run — then press one button and the rules go out to the
channel of your choice, formatted to be readable. While the event runs, the
addon watches `/roll` results from your group and calls each one a success or a
failure against your threshold.

Attendees need nothing installed. The rules arrive as ordinary chat text, and
the watcher adjudicates the plain `/roll` everyone already uses. Covered by
1375 checks across thirteen suites, run against a stub of the WoW API.

→ [Repository](https://github.com/Zethrel/Roleplay-event-helper) ·
[Releases](https://github.com/Zethrel/Roleplay-event-helper/releases)

## SayWhat

Busy roleplay hubs drown you in chat. SayWhat notices everyone who speaks
within /say range, lets you tick the handful of people you are actually talking
to, and gives them a window of their own — movable, resizable, and remembered
per character between sessions. Adding someone shows what they already said
this session rather than an empty window, and names come from Total RP 3,
MyRolePlay or XRP when a profile has been received.

Inspired by [Listener](https://www.curseforge.com/wow/addons/listener), written
from scratch with no library dependencies.

→ [Repository](https://github.com/Zethrel/say-what) ·
[Releases](https://github.com/Zethrel/say-what/releases)

---

## Installing

These are ordinary addons — extract the folder into:

```
World of Warcraft/_retail_/Interface/AddOns/
```

Download the zip from a repository's **Releases** page, not the green
*Code → Download ZIP* button. GitHub's source zip unpacks under the repository
name (`say-what-main`), and WoW requires the folder name to match the `.toc`
inside it, so the game never sees it. The release assets are built to unpack
correctly.

Restart the client afterwards rather than using `/reload`; newly added addons
are only picked up when the game launches.

## Coming up

Looking for other abandoned or broken addons worth reviving for Midnight. The
12.0 API changes — removed interface-options globals, the new secrets system,
restricted aura APIs — left a lot of good addons stranded, and plenty of them
need less work than their comment sections suggest.

Suggestions welcome; open an issue.
