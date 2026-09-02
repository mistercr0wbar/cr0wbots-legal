# BARBIE Privacy Policy

**Effective date:** 1 September 2026

**Last updated:** 1 September 2026

**Operator and privacy contact:** Derek MacIsaac, Nova Scotia, Canada

**Email:** cr0wbotsupport@gmail.com

**Support:** https://discord.gg/qkGVG3daZS

## 1. Scope and adults-only notice

This policy applies only to the **BARBIE** Discord application. BARBIE is a
separate, adults-only application for consensual adult roleplay and BDSM-themed
features. It does not cover BARNEY, other cr0wbots, Discord itself, or the
operator's personal Discord servers and communities.

**BARBIE is intended only for people aged 18 or older. Do not install, access
or use BARBIE if you are under 18. Adult features must be used only in Discord
spaces properly marked as age-restricted.**

Discord separately processes account, server and message information under
[Discord's Privacy Policy](https://discord.com/privacy). Discord's age
assurance and age-restriction controls are separate from BARBIE.

## 2. Summary

- BARBIE stores a profile tied to a Discord user ID. A profile may contain
  highly sensitive information about sexual orientation, sex life, BDSM
  preferences, limits and relationships.
- Current profiles, trust grants, ownership relationships and gag state are
  global across guilds using BARBIE rather than being stored separately for
  each guild.
- An active gag can delete a message and its attachments, transform the text
  and repost through a webhook using the member's Discord display name and
  avatar.
- In some ownership situations, the original gagged text is kept for up to 24
  hours and can be revealed to an audience selected through the gag-privacy
  feature.
- Information is stored in PostgreSQL on infrastructure hosted by Hetzner in
  Germany.
- BARBIE does not sell personal information, use it for behavioral advertising
  or send profile text to an AI provider.

## 3. Information BARBIE processes

### 3.1 Discord identifiers and guild configuration

BARBIE may process and store Discord user and guild IDs, role IDs used for
guild access, an audit-channel ID, guild access mode and feature settings.
BARBIE also receives Discord member, channel, message, display-name and avatar
information needed to respond to commands and operate enabled features.

BARBIE uses Discord's Message Content and Server Members intents. It does not
receive a user's Discord password from Discord.

### 3.2 Adult profiles

A BARBIE profile may store:

- Bot Play and D/s opt-in choices;
- pronouns or gender presentation and a GIF-gender preference;
- biography, interests, relationship and approach preferences;
- BDSM identity and position;
- sexual and romantic orientation;
- kinks and limits;
- a safeword;
- a user-selected profile color;
- a mantra and honorific used by particular gag styles; and
- counts of safeword exits and other rescues.

This information can be intimate and highly sensitive. Users should provide
only information they intentionally want BARBIE to process. Do not enter legal
names, home addresses, government identification, medical records or other
unnecessary identifying information.

Basic profile fields such as pronouns, relationship, interests and bio can be
shown in a profile card where BARBIE is used. Adult profile fields are intended
for age-restricted channels and authorized adult viewers. A user can view
their own full profile. Depending on the current relationship and trust
settings, an owner or a person granted profile-view trust may also see the
adult portion.

### 3.3 Global scope across BARBIE guilds

At the effective date of this policy, the following records are associated
with a Discord user rather than separately with each guild:

- profile and opt-in choices;
- trust grants;
- ownership relationships; and
- current gag state.

This means a profile or relationship created in one BARBIE guild can affect
what authorized users see or do in another guild that also uses BARBIE. An
active gag is looked up by Discord user ID and can operate when that user
speaks in another BARBIE guild where gags are enabled and the channel is
age-restricted. Guild configuration itself remains guild-specific.

Do not use BARBIE if you do not want this current cross-guild behavior. The
operator may change these scopes in a future version and will update this
policy when deployed behavior changes.

### 3.4 Trust and ownership

A user can grant another Discord user separate trust permissions to view a
profile, gag them or ungag them. BARBIE stores both user IDs, the selected
permissions and the time of the grant. A user can remove a trust grant.

An ownership relationship is created only after the target of a claim presses
Accept. BARBIE stores the owner and submissive Discord user IDs and the claim
time. Either participant can end the stored relationship using the available
leave or disown controls.

An ownership or trust record is an application permission. It is not evidence
of real-world consent, legal consent to sexual activity, identity, capacity or
an off-platform relationship.

### 3.5 Gags and original message text

When an active gag applies in an age-restricted channel, BARBIE:

1. receives the member's Discord message content;
2. checks for the member's stored safeword;
3. transforms the text according to the gag type;
4. deletes the original Discord message;
5. deletes any attachments, stickers or files with that original message and
   does not repost those files; and
6. reposts the transformed text through a Discord webhook using the member's
   current display name and avatar URL.

The repost is generated by BARBIE; it is not an unmodified statement by the
member even though the webhook displays their name and avatar.

If the gagged member has at least one stored owner, BARBIE also stores the
original plaintext in PostgreSQL with an opaque token, the member and guild IDs
and an expiry time. The current maximum is 24 hours. If the member has no
owner, BARBIE does not store an original plaintext copy for this feature.

The gag-privacy setting determines who can reveal the original through the
message's eye control. The levels are:

- owner only;
- owner and users to whom the member granted trust; or
- any user in that guild who may use BARBIE.

Under the current product rules, an owner selects this setting for the member.
The member can read the setting but cannot directly change it. The narrowest
level is the default.

When a gag ends through a safeword, expiry or an authorized ungag action,
BARBIE deletes stored originals for that member. The read path refuses expired
text even if the hourly physical-deletion sweep has not yet run.

### 3.6 Adult actions and media

BARBIE can post adult roleplay actions such as whip, choke, spank, peg and oil
using text and operator-managed GIF media. The target must have Bot Play
enabled. BARBIE reads the participants' Discord display names and GIF-gender
preferences to select and render the action. Output is posted to Discord.

The actions are fictional application output. They do not establish or record
real-world conduct or consent.

### 3.7 Operator-managed media

The operator can add GIF files, URLs and response phrases used by adult action
features. BARBIE stores media identifiers, action category, filename or URL,
sender/receiver category, the operator ID that added it and an added time.
Third-party websites and Discord may separately process requests for media
hosted by them.

## 4. Sources of information

BARBIE receives information:

- from Discord when users interact, send messages in contexts where enabled
  features listen, or manage a guild;
- directly from users who create profiles, opt in, grant trust, accept
  ownership, configure gag words or invoke commands;
- from guild administrators who configure access and features; and
- from the operator when media and response phrases are added.

## 5. Purposes

BARBIE processes information to:

- provide adult profiles and user-selected visibility;
- enforce Bot Play, D/s, trust and ownership permissions;
- operate, expire and revoke gags;
- provide a safeword exit and record safety counters;
- select and display adult roleplay media;
- remember guild access and feature choices;
- secure, maintain and troubleshoot the application; and
- answer support, privacy, security and safety reports.

BARBIE does not sell personal information or use it for behavioral
advertising.

## 6. Recipients and service providers

Information may be accessible to or processed by:

- **The operator**, where necessary to operate, secure, repair or support the
  application.
- **Other authorized BARBIE users**, according to profile, trust, ownership
  and gag-privacy rules described above.
- **Guild administrators**, through their Discord permissions and guild
  configuration. Guild administrators do not receive a backdoor into other
  guilds, although user-level BARBIE records currently have the cross-guild
  scope described in section 3.3.
- **Discord**, as the application platform and host of accounts, messages,
  webhooks, attachments and server content.
- **Hetzner**, which hosts the application and PostgreSQL data in Germany.
- **Google/Gmail**, when a person contacts the support email address.
- **Legal or safety authorities**, if disclosure is required by applicable law
  or reasonably necessary to respond to a valid legal process or an imminent
  safety threat.

BARBIE's application code does not currently send profiles, gagged originals
or prompts to an AI provider.

Information processed outside Canada may be subject to the laws and lawful
access processes of the country where it is processed.

## 7. Retention

| Information | Current retention |
|---|---|
| Profile and sensitive profile fields | Until a valid deletion request is completed. Turning off Bot Play or D/s, or using the current `profile delete` prefix action, clears opt-ins but does not erase the profile fields. |
| Trust grants | Until the profile owner removes the grant or a valid deletion request is completed. |
| Ownership relationships | Until either participant uses leave/disown or a valid deletion request is completed. |
| Active gag record | Until safeword, authorized ungag, expiry processing or a valid deletion request. A timed record can remain until BARBIE next processes its expiry. |
| Original gagged plaintext | Up to 24 hours, and deleted earlier when the gag ends. Expired text is not returned; an hourly sweep removes expired rows. |
| Guild configuration | Until an authorized guild-deletion request is completed. |
| Operator media and phrases | Until the operator removes or replaces them. |
| Discord messages and webhook reposts | Controlled through Discord by the guild and Discord, not by BARBIE's PostgreSQL retention. |

The public source reviewed for this policy does not establish a separate
BARBIE database-backup schedule, so this policy does not promise a specific
backup-retention or backup-deletion period. A requester may ask the operator
for current backup handling at the contact above.

Retention may be extended where reasonably necessary for security, dispute
resolution or a legal obligation. It will not be extended merely for an
unrelated new use.

## 8. Choices, access, correction and deletion

Users can:

- turn Bot Play and D/s off in their profile;
- remove a trust grant;
- leave an owner relationship without the owner's permission;
- use their stored safeword to end a gag immediately;
- leave a guild or ask its administrators to disable BARBIE; and
- request access, correction, export or deletion by emailing
  **cr0wbotsupport@gmail.com**.

The current `profile delete` prefix action is an opt-out control, not complete
erasure: it clears the two opt-ins and intentionally leaves written profile
fields available for later reactivation. A user seeking permanent erasure
must contact the operator until a dedicated in-app deletion feature is
available.

A request should identify **BARBIE**, include the requester's Discord user ID
and specify access, correction, export or deletion. Do not send a government
ID, password, authentication token, nude image, private sexual content or
unrelated message history. The operator may request a reasonable in-Discord
confirmation to prevent one person from deleting another person's data.

Deletion from BARBIE's active database does not delete messages or webhook
output already posted to Discord. Contact the relevant guild administrators or
Discord about those copies.

Depending on applicable law and location, individuals may have rights to
access, correct, delete, restrict or object to processing, withdraw consent, or
complain to a privacy regulator. These rights may be subject to lawful
exceptions.

## 9. Security

BARBIE uses operational and technical safeguards intended to match the
sensitivity of the service, including restricted host access, separation of
secrets from the public source repository, PostgreSQL access controls,
authorization checks and hard expiry checks for temporarily stored original
text. No online system is perfectly secure, and this policy does not promise
absolute security.

Security concerns should be reported privately to
**cr0wbotsupport@gmail.com**. Do not publish credentials, intimate content or
exploitable details in the support server.

## 10. Minors and prohibited use

BARBIE is not directed to minors and must not be used by or with anyone under
18. Do not use BARBIE for sexual content involving minors, grooming,
exploitation, age-roleplay involving minors, or to make adult content available
to a minor. Reports concerning minors or exploitation may be preserved and
reported where required for safety or legal compliance.

## 11. Changes

Material updates will change the date at the top and be recorded in the
[change history](../CHANGELOG.md). Where applicable law requires new notice or
consent for a materially different collection, use or disclosure—particularly
one involving sensitive profile information—the operator will provide it
rather than relying only on continued use.

## 12. Contact

Privacy questions and requests: **cr0wbotsupport@gmail.com**

General support: https://discord.gg/qkGVG3daZS
