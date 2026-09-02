# BARNEY Privacy Policy

**Effective date:** 1 September 2026

**Last updated:** 1 September 2026

**Operator and privacy contact:** Derek MacIsaac, Nova Scotia, Canada

**Email:** cr0wbotsupport@gmail.com

**Support:** https://discord.gg/qkGVG3daZS

## 1. Scope

This policy applies only to the **BARNEY** Discord application. It does not
cover BARBIE, other cr0wbots, Discord itself, or the operator's personal
Discord servers and communities.

BARNEY is installed by a server owner or another person authorized to add
Discord applications. Server administrators decide which optional features to
enable, who may operate them, and where BARNEY posts logs and transcripts.
Some BARNEY features may also be installed to a user's Discord account and
used in direct messages or group messages.

Discord separately processes information associated with Discord accounts,
servers and messages under [Discord's Privacy Policy](https://discord.com/privacy).

## 2. Summary

- BARNEY uses Discord identifiers and content needed to provide enabled
  features.
- Some information is stored in PostgreSQL on infrastructure hosted by Hetzner
  in Germany.
- Deleted-message Snipe is off by default and uses a short in-memory cache.
- Optional wardrobe requests use Anthropic for text interpretation and xAI for
  icon generation.
- Optional Last.fm features communicate with Last.fm and can store a separate
  authorization if a user expressly connects one.
- BARNEY does not sell personal information or use it for behavioral
  advertising.
- Removing BARNEY from a server does not currently erase that server's
  PostgreSQL rows automatically. Deletion can be requested using the contact
  details above.

## 3. Information BARNEY processes

### 3.1 Discord identifiers and configuration

BARNEY may process and store:

- Discord user, guild, role, channel, thread and message IDs;
- guild feature settings, access roles, filters, panels, ticket forms, log
  destinations, voice hubs, wardrobe configuration and other settings chosen
  by server administrators;
- vanity-role ownership and sharing, role-restoration snapshots, punishment
  role vaults, temporary voice-channel ownership and preferences;
- moderation and recovery state such as channel locks, lockdown snapshots,
  bulk-job progress, action reasons and the users who initiated actions; and
- service tiers, capacity grants and related administrative notes.

Discord IDs identify objects inside Discord. BARNEY does not receive a user's
Discord password from Discord.

### 3.2 Games, balances and direct-message use

BARNEY stores user and guild IDs with play-money balances, daily-claim times,
wagers, poker escrow and casino-round settlement records. Direct-message use
has a separate wallet, admission/blocking record and short-lived daily usage
counters. These records prevent duplicate payouts, restore unsettled wagers
after a crash and enforce abuse limits.

cr0wcaps are a virtual play balance. BARNEY does not use them to collect
payment-card or bank information.

### 3.3 Message content

BARNEY receives message content through Discord's Message Content intent where
needed for enabled features. Depending on server configuration and user
actions, content may be processed for:

- word filtering and channel rules;
- automatic reactions and threads;
- logging;
- Snipe;
- quote cards;
- ticket forms and transcripts;
- Last.fm trigger words; and
- wardrobe descriptions.

Processing content does not always mean it is stored in BARNEY's database:

- **Snipe:** When enabled by a server, BARNEY keeps up to the configured number
  of recently deleted messages in process memory. The default retention is two
  hours and the configurable maximum is twelve hours. The cache does not store
  attachment files, is not written to PostgreSQL and disappears on process
  restart. Server administrators can choose whether Snipe responses are
  private or public.
- **Quote cards:** BARNEY reads selected message text and Discord-hosted avatar
  or emoji images to render a quote image. The rendered card is posted to
  Discord; BARNEY does not keep a database archive of the quoted message or
  image. A user's quote preferences can follow that user between servers and
  direct messages.
- **Logs:** Copies of events or message content selected by a server's logging
  configuration are posted to Discord channels chosen by that server. Those
  copies are stored by Discord, not as a second message archive in BARNEY's
  PostgreSQL database.

### 3.4 Tickets and verification

When a server enables tickets, BARNEY can store the guild, channel, ticket
number and type; the users who opened, claimed and closed it; close reasons;
answers to configured ticket questions; and relevant timestamps.

If a ticket type keeps a transcript, BARNEY posts the channel's messages into
a Discord log channel selected by the server. Discord and that server control
the resulting Discord message. Verification-type tickets cannot be configured
to keep a transcript.

When a server uses BARNEY to organize human age verification, BARNEY stores
the **decision**, not the submitted evidence: the guild and member IDs, the
staff member who approved the decision, the route used, the minimum age
threshold, an optional staff note and the timestamp. BARNEY has no database
field for an identification image, attachment, URL, filename or document hash
and does not intentionally download or copy verification evidence. Any
material a member shows in Discord is nevertheless processed by Discord and
visible to the human server staff involved until the Discord channel or
message is removed.

### 3.5 Server clones and personal backups

At an authorized user's request, BARNEY can store a snapshot of a guild's
BARNEY settings and Discord structure, including role names and permissions,
category and channel names, channel topics and permission overwrites. These
snapshots do not contain message history or a member list.

- **Guild clones** belong to the source guild and remain until an authorized
  user deletes or replaces them. Automatic pre-restore snapshots are limited
  to the three most recent.
- **Personal backups** belong to the Discord user who created them. They can
  remain after the user leaves the source guild or the guild is deleted. The
  user can list and delete them through BARNEY.
- **Transfer codes** connect a snapshot to the Discord user who requested it
  and expire after 24 hours or earlier revocation.

### 3.6 Wardrobe

When enabled by a server, the wardrobe can process:

- a Discord user's written description of a requested role appearance;
- a derived role name, colors, style and optional icon prompt;
- the guild and user IDs involved in a wardrobe session;
- a temporary snapshot of the role being changed, including previous icon
  bytes where needed for restoration; and
- monthly guild and member usage counts.

The written description is sent to Anthropic for text interpretation. If the
user requests an icon, a derived icon prompt is sent to xAI for image
generation. Generated output is then sent to Discord to update the role. These
providers may process requests outside Canada under their own terms and
privacy policies.

### 3.7 Last.fm

Last.fm has two separate levels:

- **Link:** `/lastfm link` stores the Last.fm username supplied by the user, an
  optional trigger word, and cached artist play counts used for guild
  leaderboards and crowns. BARNEY reads listening information from Last.fm but
  does not maintain a separate archive of the user's listening history.
- **Connect:** `/lastfm connect` optionally stores a Last.fm session key that
  allows BARNEY to love and unlove tracks on that user's behalf. This is not
  required for read-only Last.fm features and does not expire automatically.

Running `/lastfm disconnect` deletes the username, trigger word, session key,
cached counts and crowns held by BARNEY. Users can separately revoke access in
their Last.fm application settings.

## 4. Sources of information

BARNEY receives information:

- from Discord when users interact with BARNEY or when enabled event listeners
  receive Discord events;
- directly from users who submit commands, forms, settings, descriptions and
  support requests;
- from server administrators who configure the application;
- from Last.fm when a user invokes an enabled Last.fm feature; and
- from Anthropic and xAI as output from an optional wardrobe request.

## 5. Purposes

BARNEY uses the information described above to:

- provide requested application features;
- remember settings and user choices;
- authorize administrative and member actions;
- prevent duplicate transactions, abuse and unsafe concurrent operations;
- recover roles, rooms, games and moderation actions after errors or restarts;
- answer support, privacy and security requests; and
- maintain the security and reliability of the service.

BARNEY does not sell personal information or use it to build advertising
profiles.

## 6. Recipients and service providers

Information may be accessible to or processed by:

- **The operator**, when necessary to operate, secure, repair or support the
  application.
- **Authorized guild administrators and staff**, through features and Discord
  channels configured by their guild. Their access is limited by Discord and
  BARNEY permissions.
- **Discord**, as the application platform and host of messages, attachments,
  accounts and server content.
- **Hetzner**, which hosts the application and PostgreSQL data in Germany.
- **Anthropic**, for optional wardrobe text interpretation.
- **xAI**, for optional wardrobe icon generation.
- **Last.fm**, when a user uses Last.fm features.
- **Google/Gmail**, when a person contacts the support email address.
- **Legal or safety authorities**, if disclosure is required by applicable law
  or reasonably necessary to respond to a valid legal process or an imminent
  safety threat.

Information hosted or processed outside Canada may be subject to the laws and
lawful access processes of the country where it is processed.

## 7. Retention

| Information | Current retention |
|---|---|
| Guild settings and feature records | Until an authorized deletion request is completed. Removing BARNEY does not currently trigger automatic deletion. |
| User feature records, balances and preferences | While needed for the feature or until a valid deletion request, subject to records that are settled or removed automatically by the feature. Leaving one guild does not delete global preferences or direct-message data. |
| Snipe content | Two hours by default, configurable up to twelve hours; memory only and also cleared by process restart. |
| Open poker escrow and casino wagers | Until settlement, refund or crash recovery. Settled records may remain temporarily to prevent duplicate settlement. |
| Guild clones | Until deleted or replaced; automatic pre-restore clones are limited to three. |
| Personal backups | Until their owning user deletes them. |
| Snapshot transfer codes | Up to 24 hours or earlier revocation. |
| Ticket records | After ticket closure until the guild's data is deleted on request. |
| Verification ticket channel | Deleted on BARNEY's configured clock, no later than 24 hours by default and possibly sooner if configured by the guild. |
| Verification decision | Until the member or guild requests removal. It may remain so a returning member can regain the verified role. |
| Last.fm information | Until `/lastfm disconnect` or a valid deletion request. |
| Wardrobe working snapshot and icon bytes | Until keep, reject, idle expiry or restart reconciliation, except the minimal session row needed to keep an active stall available. |
| Wardrobe usage meters | By calendar month. Older monthly rows can remain as usage history until deletion is requested. |
| Discord logs, transcripts and bot messages | Controlled through Discord by the guild and Discord, not by BARNEY's PostgreSQL retention. |
| Database backups | The current job keeps 30 daily database backups and 12 first-of-month backups. Backups are restricted operational copies and age out through rotation. A deletion from the live database may remain in a backup until that backup rotates out and will not be restored for ordinary use. |

Retention may be extended where reasonably necessary for security, dispute
resolution or a legal obligation. It will not be extended merely for an
unrelated new use.

## 8. Choices, access, correction and deletion

Depending on the feature, users can:

- ask a guild administrator to disable an optional feature;
- use `/lastfm disconnect` to remove all BARNEY-held Last.fm information;
- delete their own personal snapshot backups;
- change quote preferences and other user settings in BARNEY;
- leave a server or ask its owner to remove BARNEY; and
- request access, correction, export or deletion by emailing
  **cr0wbotsupport@gmail.com**.

A request should identify **BARNEY**, include the requester's Discord user ID
and, for guild-level requests, the guild ID and the requester's authority to act
for that guild. Do not send passwords, bot tokens, `.env` files, government
identification or unrelated private messages. The operator may request a
reasonable in-Discord confirmation to prevent one person from deleting another
person's data.

Deletion from BARNEY's active database does not delete copies already posted
to Discord channels. Users should also contact the relevant guild
administrators or Discord about those copies. Deleted active-database data may
remain in restricted backups until rotation as described above.

Depending on applicable law and location, individuals may have rights to
access, correct, delete, restrict or object to processing, withdraw consent, or
complain to a privacy regulator. These rights may be subject to lawful
exceptions.

## 9. Security

BARNEY uses operational and technical safeguards intended to match the nature
of the service, including restricted host access, separation of secrets from
the public source repository, database access controls, limited backup file
permissions and feature-level authorization checks. No online system is
perfectly secure, and this policy does not promise absolute security.

Security concerns should be reported privately to
**cr0wbotsupport@gmail.com**. Do not publish credentials or exploitable details
in the support server.

## 10. Age

BARNEY is a SFW application and is not intended for anyone below the minimum
age required to use Discord in their country. Guild owners remain responsible
for applying Discord age restrictions to their own community content. BARNEY's
verification workflow does not make BARNEY an identity-verification service
and does not transfer a verification decision between unrelated guilds.

BARBIE and any adult applications have separate policies and are not covered
here.

## 11. Changes

Material updates will change the date at the top and be recorded in the
[change history](../CHANGELOG.md). Where applicable law requires new notice or
consent for a materially different collection, use or disclosure, the operator
will provide it rather than relying only on continued use.

## 12. Contact

Privacy questions and requests: **cr0wbotsupport@gmail.com**

General support: https://discord.gg/qkGVG3daZS
