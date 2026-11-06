# BARCHORD Privacy Policy

**Effective date:** 6 November 2026

BARCHORD plays music and reads eligible chat aloud in private Discord servers. This
policy covers BARCHORD and its voice worker accounts. Derek MacIsaac operates BARCHORD
from Nova Scotia, Canada. For privacy questions or requests, email
**cr0wbotsupport@gmail.com**.

## 1. Discord messages and voice

BARCHORD receives messages in Discord server channels it can access so it can recognize
commands addressed to it and check which messages can be read aloud. It also receives
slash command options and button actions. BARCHORD uses Discord server, channel, user
and role IDs and current voice channel membership to check permissions and direct
playback.

An authorized member can start reading with `/join` or the reading controls. A server
can also enable autojoin when an eligible member types in their voice channel's chat.
While reading is active, BARCHORD can read from enabled voice channel chat and from a
designated text channel if the server has set one. It checks that the author is in the
voice channel and honors server reading rules and the author's opt-out. It can speak
the author's display name or chosen spoken name and use names in mentions, attachment
types and sticker names to describe the message.

BARCHORD synthesizes speech on its host and keeps chat text and generated speech only
in working memory. It uses its voice connection for outgoing playback to the people in
the room. Audit records can include the author and message IDs, message length, time
and action.

## 2. Music requests

BARCHORD sends music search terms to YouTube or SoundCloud, including some partial
searches as you type in `/play`. When you submit a supported link, BARCHORD uses the
public link or track identifier for lookup. Spotify supplies track and artist
information for matching. BARCHORD retrieves public audio from supported sources,
including SoundCloud and Bandcamp. For YouTube tracks, it may send the public link
or video ID to CNVMP3, Tunelio if configured, or Samplecut to obtain playable audio.

BARCHORD stores track information, queue order, requester IDs and playback state so it
can manage the queue and resume sessions after interruptions. Track information and the
requester's Discord identity can appear in queue and playback panels visible to people
with access to the channel.

## 3. Settings, hosting and support

BARCHORD saves server settings, such as permitted roles and reading rules. It saves
your speech voice, rate and opt-out by Discord account across servers, and your chosen
spoken name separately for each server. It uses audit records and service logs to
diagnose problems and operate the bot.

BARCHORD's database, logs and local backups are on infrastructure hosted by Hetzner in
Germany. The database and its backups are restricted to operational accounts. The
operator accesses stored records to maintain, secure and support BARCHORD. Where a
server uses BARNEY's reading controls, the two bots exchange the relevant server,
channel and user IDs, control actions and reading state on the same host. Discord
handles its own copies of messages and bot posts and provides voice transport.
[Discord Privacy Policy](https://discord.com/privacy)

If you email support, Gmail processes your email address and the information you
include. The operator uses that information to respond and resolve the request. The
operator may disclose information when required by law.

## 4. How long information is kept

- **Queues and playback.** BARCHORD removes queue entries as they are played or
  cleared. A queue interrupted by a disconnect can generally be resumed for 15 minutes.
  A cleanup job clears stale saved queues after 24 hours. Some session metadata can
  remain after the queue expires.
- **Settings and audits.** Personal preferences, server settings and database audit
  records have no fixed automatic expiry. Server settings can remain after a server
  removes BARCHORD. Service logs rotate under the host's journal settings.
- **Cached music.** Audio files are kept in a separate cache. BARCHORD evicts cached
  files and their cache records as space is needed.
- **Database backups.** The backup job keeps 30 daily and 12 monthly copies for
  disaster recovery. Data erased from the live database may remain in a restricted
  backup until that copy rotates out.

## 5. Privacy choices and requests

Your messages can be read by default when they meet the rules above. In `/barchord` →
**You**, select **Do not read me** to stop BARCHORD from reading your messages across
servers and cancel your queued or current speech. Select **Forget me** and confirm to
remove your saved speech preferences and your Discord user ID from attribution in
BARCHORD's live database across servers. This also resets your opt-out. Select
**Do not read me** again afterward if you want to keep reading off.

To ask for access, a copy, correction or deletion of your data, email
**cr0wbotsupport@gmail.com** with the subject `BARCHORD privacy request`. Include your
Discord user ID and the server ID if relevant. For a server-wide request, explain how
you are authorized to act for the server. The operator may ask you to confirm your
identity through Discord. For copies in a Discord channel, contact the server's
administrators or Discord.

You can use the same address to report security issues, abuse or other problems with
BARCHORD. Include enough information to identify the issue and leave out passwords,
tokens and unrelated private messages.
