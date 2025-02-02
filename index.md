---
layout: home
---

Compendium of nostr clients and known features.

Contribute updates on github: <https://github.com/nostorg/clients>

<div class="bigtable">
<table>
  {% for row in site.data.clients %}
    {% if forloop.first %}
    <tr>
      {% for pair in row %}
        <th>{{ pair[0] }}</th>
      {% endfor %}
    </tr>
    {% endif %}

    {% tablerow pair in row %}
      {{ pair[1] }}
    {% endtablerow %}
  {% endfor %}
</table>
</div>

## Legend

- [NIPs](https://github.com/nostr-protocol/nips)
- ✅ : mostly supported
- 🟡 : partially supported
- ❌ : mostly not supported
- ⚡ : paid feature
- `?` : reviewed but inconclusive
- <code>&nbsp;</code> : not yet reviewed

## Criteria for ✅

Any column with at least one 🟡 entry should have some criteria listed here.

- Zaps: Can view who zapped what amounts on notes; can zap notes and profiles via integrated wallet, external application, or QR code.
- Reactions: Can view who reacted with which reactions; can react with any unicode emoji.
- Event Deletion: Can delete own notes and undo reactions by deletion.
- Direct Messages: Can view and decrypt all past conversations; can encrypt and send new messages.
- Local Feeds: Can view all recent notes from connected relays and filter by relay.
- Algorithmic Feeds: Can view custom feeds determined by some open source or configurable algorithm (e.g. "trending").
- Mute List: Reads from and writes to the kind 10000 list, not a kind 30000 parameterized list.
- Pins: Reads from and writes to the kind 10001 list, not a kind 30001 parameterized list.
- Bookmarks: Reads from and writes to a kind 30001 parameterized list.
- Relay List: Reads from and writes to the kind 10002 relay list; DOES NOT write relay list changes to the kind 3 contact list; shows relay lists for other users; can toggle read/write access for each connected relay.
- Event Relays: Shows all connected relays where an event exists.
- Relay Info: Shows all available relay metadata for all connected relays.
- Long-form Content: Properly renders markdown; updated events are fully replaced or the update history is clearly indicated.
- Search: On connected relays, returns any existing user by username or NIP-05, and returns any existing note by content.
- Push Notifications: Received on device without requiring the client software to be actively running.
- Machine Translation: Can do offline translation of notes with configurable language models.
- Multiple Accounts: Saves multiple profiles to switch between views or logins for multiple accounts with public keys, private keys, or extension (NIP-07).
- macOS: Has a fully native desktop macOS app, not just a mobile app that can run on Apple Silicon.

## Similar projects

- <https://github.com/aljazceru/awesome-nostr>
- <https://github.com/vishalxl/Nostr-Clients-Features-List>
- [Nostr Client Comparison Sheet (Google Docs)](https://docs.google.com/spreadsheets/d/1GjfN_eMiEywqXfKFHZMw4rLnoQLBXYEyl2NCEtsCXWw/edit)
- <https://www.nostrapps.com/>
- <https://nostrapp.link/>
