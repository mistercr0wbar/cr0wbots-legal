# BARCHORD Privacy Policy

**Effective date:** 6 November 2026

**Last updated:** 13 November 2026

BARCHORD plays music and reads eligible chat aloud in Discord servers where it
is installed. This policy covers BARCHORD and its voice worker accounts.
Derek MacIsaac operates BARCHORD from Nova Scotia, Canada. For privacy
questions or requests, email **cr0wbotsupport@gmail.com**.

## 1. Discord messages and voice

BARCHORD receives messages in Discord server channels it can access so it can recognize
commands addressed to it and check which messages can be read aloud. It also receives
slash command options and button actions. BARCHORD uses Discord server, channel, user
and role IDs and current voice channel membership to check permissions and direct
playback.

An authorized member can start reading with `/read`, **Read chat**, or the
**Reading off** control on the player strip. The strip shows **Reading on** or
**Reading off**. Use `/join` to connect the player without starting a reading
session. A server can also enable
automatic reading when an eligible member types in their voice channel's chat.
An additional text channel configured by the server can supply messages to an
active session only if every member can read that channel and the channel has
no age restriction. BARCHORD checks those permissions again before playback
and discards queued or current speech from that source if it becomes restricted
or is removed. BARCHORD checks that the author is in the voice channel and
applies the server's reading rules and the author's opt-out. It can say the
author's display name or chosen spoken name and describe mentions, attachment
types and stickers.

BARCHORD synthesizes speech on its host. Text used for reading aloud and the
generated speech stay in working memory. BARCHORD plays that audio to the
people in the voice channel. Audit records can include the author and message
IDs, message length, time and action.

The voice picker can generate a fixed sample on the host and send it as a private
Discord attachment. For up to three minutes after generating it, you can choose
**Hear in VC** to play the sample to people in your current voice channel.

## 2. Music requests

BARCHORD sends music search terms to Deezer, YouTube or SoundCloud for
catalogue lookup, depending on the server's settings. When you type in `/play`,
BARCHORD can also send partial search text to the selected catalogue or Google's
YouTube autocomplete service. When you submit a supported link, BARCHORD uses
the public link or track identifier for lookup. Spotify supplies track and
artist information for matching to a playable source. BARCHORD uses Deezer
track identifiers to retrieve audio from Deezer and also retrieves audio from
SoundCloud and Bandcamp. For YouTube tracks, BARCHORD can send the public link
or video ID to CNVMP3 or Samplecut to obtain playable audio.

**Recent** suggestions use your server's queue and recently started tracks.
These suggestions show track information without identifying the requester.
BARCHORD uses a shared audio cache for playback.

BARCHORD stores track information, queue order, requester IDs, voice-channel
connection state and playback state so it can manage the player and resume
sessions after interruptions. The submitted link or search phrase can be kept
with a track in queue and cache metadata. Queue and playback panels can show
track information and the requester's Discord identity. The compact controls
are posted in the voice channel's chat, and expanded controls can be opened
privately.

### Personal audio and Last.fm

BARCHORD stores your personal music volume and five-band EQ under your Discord
user ID. For a shared session it saves who started the session and which sound
settings it applied. Loudness measurements identify cached audio by content
hash. Automatic voice status can display the current artist and song. BARCHORD
saves the previous text so it can restore it after playback. Manual status
edits take priority.

In BARCHORD’s `/lastfm`, linking stores your Last.fm username and optional
trigger word. BARCHORD reads listening information from Last.fm and caches
artist counts and crowns for server boards. A posted card can retain its
track, artist and Discord message ID so its buttons can act on the right song.
Connecting stores a Last.fm session key so BARCHORD can love or unlove a track
on your behalf and submit scrobbles if you separately enable that setting.

Scrobbling is off by default. For opted-in listeners, BARCHORD measures music
it delivers while they are present and not deafened. It stores Discord user,
server and channel IDs, track metadata, listening duration, original start
time, a consent identifier and submission state. It sends track and listening
details to Last.fm. The private heart works independently of scrobbling.
[Last.fm Privacy Policy](https://www.last.fm/legal/privacy)

Barney is an affiliated cr0wbots bot. With **Share account info with Barney**
enabled, BARCHORD shares your Last.fm username and linked status with Barney
when he requests them for your settings. The setting is on by default and
can be turned off under **Your account** at any time. BARCHORD keeps your
authorization, trigger and listening records.

## 3. Settings, hosting and support

BARCHORD saves server settings, such as permitted roles and reading rules. It saves
your speech voice, rate and opt-out by Discord account across servers, and your chosen
spoken name separately for each server. It uses audit records and service logs to
diagnose problems and operate the bot.

BARCHORD's database, logs and local backups are on infrastructure hosted by Hetzner in
Germany. The database and its backups are restricted to operational accounts. The
operator accesses stored records to maintain, secure and support BARCHORD. In
BARNEY temporary voice rooms, the two bots coordinate their controls over a local
connection on the same host. They exchange server, channel, message and relevant
user IDs, control actions, reading and player status, and track and requester
information for playback or queue controls. BARCHORD handles chat text and
speech synthesis. Discord handles its copies of messages, bot posts and preview
attachments, and provides voice transport.
[Discord Privacy Policy](https://discord.com/privacy)

If you email support, Gmail processes your email address and the information you
include. The operator uses that information to respond and resolve the request. The
operator may disclose information when required by law.

## 4. How long information is kept

- **Queues and playback.** BARCHORD removes queue entries as they are played or
  cleared. A queue interrupted by a disconnect can generally be resumed for 15 minutes.
  A cleanup job clears stale saved queues after 24 hours. Some session metadata can
  remain after the queue expires.
- **Recent suggestions.** BARCHORD keeps up to 25 distinct recently started YouTube
  tracks per server for autocomplete. It stores the track information and when it
  last started.
- **Settings and audits.** Personal preferences, server settings and database audit
  records have no fixed automatic expiry. Server settings can remain after a server
  removes BARCHORD. Service logs rotate under the host's journal settings.
- **Cached music.** BARCHORD keeps audio files and track metadata in a shared
  cache and evicts them as space is needed.
- **Last.fm listening.** Progress and queued submission records expire after
  14 days. BARNEY removes submission receipts older than 14 days when handling
  further submissions. Withdrawal or account erasure can remove them sooner.
  BARCHORD removes pending local listening data when it verifies consent was
  withdrawn. BARNEY checks consent again before a queued submission. An opaque
  revoked consent identifier can remain after erasure to prevent an old opt-in
  from recreating erased history. Last.fm keeps its own submitted records.
- **Database backups.** The backup job keeps 30 daily and 12 monthly copies for
  disaster recovery. Data erased from the live database may remain in a restricted
  backup until that copy rotates out.

## 5. Privacy choices and requests

Your messages can be read by default when they meet the rules above. In `/barchord` →
**User**, select **Do not read me** to stop BARCHORD from reading your messages across
servers and cancel your queued or current speech. Select **Forget me** and confirm to
remove your saved speech/music preferences, listening checkpoints and queued
submissions, and your Discord user ID from attribution in
BARCHORD's live database across servers. This also resets your opt-out. Select
**Do not read me** again afterward if you want to keep reading off.

Use BARCHORD’s **/lastfm → Your account** to turn off scrobbling, stop
sharing with Barney or choose **Delete everything** to remove your link,
authorization, trigger, queued listening and cached counts and crowns. Use
Last.fm’s application settings to revoke access and its own controls to remove
records already submitted there.

To ask for access, a copy, correction or deletion of your data, email
**cr0wbotsupport@gmail.com** with the subject `BARCHORD privacy request`. Include your
Discord user ID and the server ID if relevant. For a server-wide request, explain how
you are authorized to act for the server. The operator may ask you to confirm your
identity through Discord. For copies in a Discord channel, contact the server's
administrators or Discord.

You can use the same address to report security issues, abuse or other problems with
BARCHORD. Include enough information to identify the issue and leave out passwords,
tokens and unrelated private messages.
