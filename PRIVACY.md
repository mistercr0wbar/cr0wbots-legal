# BARNEY Privacy Policy

**Effective: 28 August 2026**  
**Operator:** Derek MacIsaac, Nova Scotia, Canada  
**Contact:** cr0wbotsupport@gmail.com  
**Support:** https://discord.gg/qkGVG3daZS

This policy is for the **BARNEY** Discord application only. It is not a
policy for the operator’s personal Discord servers, and it is not a policy
for other cr0wbots (including BARBIE).

BARNEY is a server-management bot. A **server owner** (or someone with
permission to add apps) invites it. Members of that server then use whatever
features the owner has turned on.

Discord is a separate company. Discord’s own privacy policy applies to
your Discord account: https://discord.com/privacy

---

## What BARNEY stores

All of this lives in a PostgreSQL database on a server the operator
runs at **Hetzner in Germany**, unless noted. That means personal
information **leaves Canada** and may be subject to German / EU law
and foreign legal process. If the wardrobe is enabled, descriptions
(and icon prompts) also go to a **language-model provider outside
Canada** (currently Anthropic in the United States).

| What | Why |
|---|---|
| Discord **guild (server) ID** | One settings blob per server |
| Per-server **settings** (JSON) | Feature flags, access roles, vanity tiers, filter lists, panel templates, log-channel IDs, wardrobe hub, temp-voice hub, and similar configuration the owner set in `/admin` |
| Discord **user IDs** tied to vanity ownership, shares, role snapshots, economy balances, poker escrow, casino round IDs, temp-voice rooms/preferences, wardrobe sessions, capacity grants | To make those features work |
| **Wardrobe icon bytes** | Raw image data (`BYTEA`) for the previous vanity badge so a rejected try-on can restore it. Generated icons, when that phase is on, are the same kind of data. |
| **Voice channel joins/leaves** | BARNEY watches voice-state changes in real time so temporary rooms can be created and torn down. It does not use Presence intent (online/offline/status). |
| **Message content**, only when a feature that needs it is on | Word filter, channel rules, auto-react, auto-threads, snipe, quote, wardrobe descriptions |
| **Snipe cache** | Recently deleted messages in a channel, **in memory only**, for a few hours, never written to the database. Dies when the process restarts. Off unless the owner enables Snipe. |
| **Logs BARNEY posts** | Copies of events (joins, deletes, “BARNEY did X”) go into **Discord channels the owner chose**. Those copies live on Discord, not as a second archive in our database. |
| **Wardrobe descriptions** | If the owner enables the wardrobe, the text you type in the stall may be sent to a **third-party language-model provider** so BARNEY can hang a look. That provider sees the description (and an icon prompt, if any), not your Discord password. |

BARNEY does **not** store your Discord password, email, phone number, IP
address, payment cards, or government ID. It does not sell personal
information.

Message Content and Server Members are **privileged Discord intents**. They
exist so automod, logging, vanity, and similar features can see members and
message text. Presence intent is not used.

---

## Who can see it

- The **operator**, to run and repair the bot.
- **Server owners / configured staff**, via the features they turned on
  (they can already see their own Discord; BARNEY does not give them a
  backdoor into other servers).
- A **language-model provider outside Canada**, only for wardrobe text
  and icon prompts, only if wardrobe is enabled on that server.
- **Discord**, as the platform. We send API calls to Discord to create
  roles, post panels, delete filtered messages, and so on.

Data is not sold. It is not used for advertising.

---

## How long

| Kind | Retention |
|---|---|
| Server settings and feature rows | Until the owner asks for deletion, or until an automated wipe exists and the bot is removed from that server |
| Snipe | Hours, memory only |
| Poker escrow / open casino wagers | Until the hand/round settles or crash-recovery refunds them |
| Wardrobe try-on snapshot (colours, name, icon bytes) | Cleared on Keep, Reject, idle expiry, or restart reconcile. A thin session row (user ID + stall thread ID) can remain so the stall stays open until the stall itself ends. |
| Discord log messages | Controlled by that server’s Discord, not by us |

**Kicking BARNEY does not yet automatically erase the database rows for
that server.** That wipe is planned. Until it ships, email
cr0wbotsupport@gmail.com or ask in https://discord.gg/qkGVG3daZS.
You will get a human reply.

A member who wants **their** user ID removed from economy, vanity
ownership, and wardrobe rows can use the same contact. Server-level
settings belong to the owner.

---

## Age

BARNEY is a **SFW** application on Discord’s 13+ platform. The operator’s
personal Discord servers (including any 19+ lore/NSFW spaces) are
**not** BARNEY’s product and are not this policy.

Separate adult applications (for example BARBIE) have or will have their
own terms. Do not treat this policy as covering them.

Server owners are responsible for their own Discord age gates and for
how they use snipe, logging, and filters in their community.

---

## Your choices

- Don’t use a feature (or ask the owner to turn it off). Snipe, wardrobe,
  and the filter only run where enabled.
- Leave the server, or ask the owner to kick BARNEY.
- Email **cr0wbotsupport@gmail.com** or ask in the support server
  (https://discord.gg/qkGVG3daZS) for access or deletion of data BARNEY
  stored about you.

Canadian privacy law (PIPEDA) may apply to this operation. If you are in
the EU/UK, you may have additional rights (access, correction, erasure,
complaint to a supervisor). Email first; we will not pretend to be a
law firm.

---

## Changes

Updates will be dated at the top of this file. Continued use of BARNEY
after a change means the new text applies.
