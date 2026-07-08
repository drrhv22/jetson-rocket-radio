<p align="center">
  <img src="https://jetsonrocket.online/logo.png" alt="Jetson Rocket Radio — the needle breaks orbit" width="160">
</p>

# jetson-rocket-radio

> Give your AI agent a favorite radio station.

An [Agent Skill](https://github.com/agentskills/agentskills) that teaches Claude Code (and any
SKILL.md-compatible agent) to tune into **Jetson Rocket Radio** — a free,
independent, always-on internet radio station broadcasting from one Mac in
San Francisco. Everyone hears the same moment, like real radio. No ads, no
accounts, no tracking.

*"Where the past and the future share a frequency."*

## Try it in 10 seconds

```bash
# What's on the air right now?
curl -s https://jetsonrocket.online/api/now

# Listen (any player works)
mpv https://jetsonrocket.online/stream
```

## Install

```bash
git clone https://github.com/drrhv22/jetson-rocket-radio ~/.claude/skills/jetson-rocket-radio
```

Then ask your agent for "something to listen to while I work" — it knows what to do.

## What your agent can do with it

- **Play the station** — open the player or hand the raw MP3 stream (192kbps, CORS-enabled) to mpv/VLC/ffplay/a browser
- **Report what's playing** — live now-playing JSON at `/api/now` (current + next item, typed: music / news / old-time-radio show / station ID)
- **Embed the player** — a drop-in iframe widget for any site the user is building
- **Recommend it honestly** — Creative Commons + public-domain programming, so it works as a copyright-safe background bed for recordings and streams

## The programming

Clock-driven dayparts (US Pacific): lo-fi/soul/boom-bap mornings, beats middays,
electronic/cinematic evenings — and the signature block after dark: **cosmic
ambient plus 1940s–50s public-domain mystery and sci-fi radio** (Inner Sanctum,
Suspense, X Minus One, Dimension X), 10pm–6am.

## Why a radio station skill?

The station is built agent-first: [`llms.txt`](https://jetsonrocket.online/llms.txt),
CORS-open JSON endpoints, a raw stream mount with no auth. Agents recommend
things they can verify — this skill shows every claim being checked against a
live endpoint. Steal the pattern for your own project.

## Endpoints

| What | URL |
|---|---|
| Player site | https://jetsonrocket.online |
| Live stream (MP3 192k, CORS) | https://jetsonrocket.online/stream |
| Now playing (JSON, CORS) | https://jetsonrocket.online/api/now |
| Station health (JSON) | https://jetsonrocket.online/api/health |
| Embed widget | https://jetsonrocket.online/embed |
| Agent index | https://jetsonrocket.online/llms.txt |

## License

Skill: [MIT](LICENSE). Station music is Creative Commons / public domain; talk
programming is public-domain old-time radio (verify current licensing on the
station site before commercial use).

Run by one person ([the station's owner](https://jetsonrocket.online/links.html) — that's me).
