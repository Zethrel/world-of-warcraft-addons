# World of Warcraft AddOns

An index of the WoW addons I maintain. Each one lives in its own repository —
this is just the front door.

| AddOn | What it does | Retail | Repository |
| --- | --- | --- | --- |
| **Eloquence** | Linguistic chat filters and racial dialects for roleplay | 12.0.7 | [Zethrel/Eloquence](https://github.com/Zethrel/Eloquence) |
| **KillThemAll** | Randomly plays Old Gods whispers, like the sha-touched weapons of MoP | 12.0.7 | [Zethrel/kill-them-all-addon](https://github.com/Zethrel/kill-them-all-addon) |

## Eloquence

A revival of the classic roleplaying chat addon, rebuilt for modern retail. It
gives every speaker an accent or dialect based on their race, and layers
linguistic filters over the chat you read — correcting spelling, expanding
acronyms, censoring profanity, and dragging modern turns of phrase into
something that sounds like it belongs in Azeroth.

Written from scratch. MIT licensed.

→ [Repository](https://github.com/Zethrel/Eloquence) · [Releases](https://github.com/Zethrel/Eloquence/releases)

## KillThemAll

Randomly plays Old Gods whispers audio files, reproducing the effect of the
sha-touched weapons of Mists of Pandaria. Y'Shaarj, C'Thun, Yogg-Saron and
Il'Gynoth are all available, with a configurable delay and sound channel.

Originally by [Thex](https://github.com/Thex-PiedDroit/KillThemAll)
([CurseForge](https://www.curseforge.com/wow/addons/killthemall)), which stopped
at Interface 100207 (Dragonflight 10.2.7). This fork updates it for Midnight —
bumping the `.toc` alone was not enough, because three globals the addon calls
were removed from retail in 11.0. MIT licensed, as upstream.

→ [Repository](https://github.com/Zethrel/kill-them-all-addon) · [Releases](https://github.com/Zethrel/kill-them-all-addon/releases)

## Installing

These are ordinary addons — extract the folder into:

```
World of Warcraft/_retail_/Interface/AddOns/
```

Restart the client afterwards rather than using `/reload`; newly added addons
are not picked up by a reload.

## Coming up

Looking for other abandoned or broken addons worth reviving for Midnight. The
12.0 API changes — removed interface-options globals, the new secrets system,
restricted aura APIs — left a lot of good addons stranded, and plenty of them
need less work than their comment sections suggest.

Suggestions welcome; open an issue.
