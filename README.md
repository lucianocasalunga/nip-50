# NIP-50 · Search Capability on LiberNet

> Search Capability, as used by the **LiberNet** apps.

**Official spec:** [nostr-protocol/nips · 50.md](https://github.com/nostr-protocol/nips/blob/master/50.md)
**Status upstream:** `draft` `optional` `relay`
**Maintainer of this repo:** Luciano "Barak" Casalunga ([@lucianocasalunga](https://github.com/lucianocasalunga)) · [libernet.app](https://libernet.app)

## My role

I took part in the creation of NIP-50, and it runs across the LiberNet apps.

## Why NIP-50 matters for LiberNet

Search is how people find each other and find content on LiberNet. NIP-50 adds a `search` field to normal Nostr filters, so the same `REQ` that loads a feed can also search notes and profiles.

## How it works (quick reference)

| Field / extension | Purpose |
|-------------------|---------|
| `"search": "<text>"` | Free-text query inside a `REQ` filter |
| `include:spam` | Turn off spam filtering |
| `domain:<domain>` | Only users with a matching NIP-05 domain |
| `language:<code>` | Only one language (e.g. `language:pt`) |
| `sentiment:<value>` | negative / neutral / positive |
| `nsfw:<true/false>` | Include or exclude NSFW |

Results come sorted by relevance, not by date. LiberNet announces `50` in its NIP-11 `supported_nips`.

### Example: searching Portuguese notes about Bitcoin

```json
["REQ", "busca", {"kinds": [1], "search": "bitcoin language:pt", "limit": 20}]
```

## Related LiberNet NIPs

[NIP-43](https://github.com/lucianocasalunga/nip-43) · [NIP-45](https://github.com/lucianocasalunga/nip-45) · [NIP-66](https://github.com/lucianocasalunga/nip-66) · [NIP-67](https://github.com/lucianocasalunga/nip-67) · [NIP-70](https://github.com/lucianocasalunga/nip-70) · [NIP-77](https://github.com/lucianocasalunga/nip-77) · [NIP-86](https://github.com/lucianocasalunga/nip-86) · [NIP-95 (my proposal)](https://github.com/lucianocasalunga/nip-95)

---
Nostr since 2021 · Part of the LiberNet ecosystem
