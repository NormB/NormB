<div align="center">

# Norm Brandinger

**SIP and real-time media infrastructure — in Rust and C**

<a href="https://github.com/OpenSIPS/opensips/pulls?q=is%3Apr+author%3ANormB+is%3Amerged"><img alt="OpenSIPS" src="https://img.shields.io/badge/OpenSIPS-1a5f7a?style=flat-square"></a>
<a href="https://github.com/kamailio/kamailio/pulls?q=is%3Apr+author%3ANormB+is%3Amerged"><img alt="Kamailio" src="https://img.shields.io/badge/Kamailio-2b6cb0?style=flat-square"></a>
<a href="https://github.com/signalwire/freeswitch/pulls?q=is%3Apr+author%3ANormB+is%3Amerged"><img alt="FreeSWITCH" src="https://img.shields.io/badge/FreeSWITCH-0b5f73?style=flat-square"></a>
<a href="https://github.com/asterisk/asterisk/issues?q=author%3ANormB"><img alt="Asterisk" src="https://img.shields.io/badge/Asterisk-c8412a?style=flat-square"></a>
<img alt="rtpengine" src="https://img.shields.io/badge/rtpengine-3c6e57?style=flat-square">
<img alt="Rust" src="https://img.shields.io/badge/Rust-b7410e?style=flat-square&logo=rust&logoColor=white">
<img alt="C" src="https://img.shields.io/badge/C-4b5563?style=flat-square&logo=c&logoColor=white">

</div>

I build and debug the parts of telephony that carry actual calls: SIP proxies,
media relays, and the tooling around them. I have been contributing upstream
since 2006. Most of my work is on **OpenSIPS**,
**Kamailio**, **rtpengine**, **FreeSWITCH** and **Asterisk** — upstream where it belongs, and
in my own tools where nothing suitable existed.

---

### Building

| Project | | |
|---|---|---|
| **[sipnab](https://github.com/NormB/sipnab)** · [sipnab.com](https://sipnab.com) | SIP & RTP capture, analysis and security. One binary, one dependency (libpcap). | [![stars](https://img.shields.io/github/stars/NormB/sipnab?style=flat-square&label=%E2%98%85&labelColor=1c1917&color=0b7285)](https://github.com/NormB/sipnab) [![release](https://img.shields.io/github/v/release/NormB/sipnab?style=flat-square&labelColor=1c1917&color=555)](https://github.com/NormB/sipnab/releases) |
| **[opensips-lsp](https://github.com/NormB/opensips-lsp)** | Language server for OpenSIPS routing scripts — completion, diagnostics, go-to-definition. | [![stars](https://img.shields.io/github/stars/NormB/opensips-lsp?style=flat-square&label=%E2%98%85&labelColor=1c1917&color=0b7285)](https://github.com/NormB/opensips-lsp) |
| **[kamailio-lsp](https://github.com/NormB/kamailio-lsp)** | The same, for Kamailio configuration files. | [![stars](https://img.shields.io/github/stars/NormB/kamailio-lsp?style=flat-square&label=%E2%98%85&labelColor=1c1917&color=0b7285)](https://github.com/NormB/kamailio-lsp) |
| **[devstack-core](https://github.com/NormB/devstack-core)** | Local VoIP development infrastructure — Docker, Postgres, MongoDB, RabbitMQ, Prometheus, Grafana. | [![stars](https://img.shields.io/github/stars/NormB/devstack-core?style=flat-square&label=%E2%98%85&labelColor=1c1917&color=0b7285)](https://github.com/NormB/devstack-core) |
| **[voip-stack](https://github.com/NormB/voip-stack)** | Production-shaped OpenSIPS + Asterisk + rtpengine deployment. | [![stars](https://img.shields.io/github/stars/NormB/voip-stack?style=flat-square&label=%E2%98%85&labelColor=1c1917&color=0b7285)](https://github.com/NormB/voip-stack) |
| **[homebrew-tap](https://github.com/NormB/homebrew-tap)** | `brew install NormB/tap/sipnab` | |
| **[mod_mosquitto](https://github.com/freeswitch/mod_mosquitto)** | FreeSWITCH event handler bridging FreeSWITCH events to an MQTT broker. Written from scratch; maintained upstream under the FreeSWITCH org. | [![stars](https://img.shields.io/github/stars/freeswitch/mod_mosquitto?style=flat-square&label=%E2%98%85&labelColor=1c1917&color=0b7285)](https://github.com/freeswitch/mod_mosquitto) |

### Upstream

Merged pull requests. Every count links to the search that produces it.

| Project | Merged |
|---|---|
| [OpenSIPS/opensips](https://github.com/OpenSIPS/opensips/pulls?q=is%3Apr+author%3ANormB+is%3Amerged) | **45** |
| [freeswitch/mod_mosquitto](https://github.com/freeswitch/mod_mosquitto/pulls?q=is%3Apr+author%3ANormB+is%3Amerged) | **5** |
| [kamailio/kamailio](https://github.com/kamailio/kamailio/pulls?q=is%3Apr+author%3ANormB+is%3Amerged) | **4** |
| [signalwire/freeswitch](https://github.com/signalwire/freeswitch/pulls?q=is%3Apr+author%3ANormB+is%3Amerged) | **4** |
| [nats-io/nats.c](https://github.com/nats-io/nats.c/pulls?q=is%3Apr+author%3ANormB+is%3Amerged) | **2** |
| [valkey-io/valkey-admin](https://github.com/valkey-io/valkey-admin/pulls?q=is%3Apr+author%3ANormB+is%3Amerged) | **1** |

### Currently

- **sipnab** — deepening protocol coverage (SIP, SDP, RTP/RTCP, STUN/TURN, TLS/DTLS) and the MCP server that exposes it to agents
- **opensips-lsp / kamailio-lsp** — bringing real editor tooling to SIP routing scripts, which have never had any
- **OpenSIPS upstream** — bug reproduction and fixes, mostly around dialog state, TLS and media
- **devstack-core** — making a full VoIP stack reproducible on an ARM laptop

### Tech & focus

```
SIP stacks     OpenSIPS · Kamailio · Asterisk · FreeSWITCH
Media          rtpengine · RTP/RTCP · SRTP · SDP · codecs
Languages      Rust · C · Shell · Python
Data & bus     Valkey/Redis · PostgreSQL · MongoDB · RabbitMQ · NATS
Ops            Docker · Prometheus · Grafana · HAProxy · libpcap
Testing        SIPp · tcpdump/pcap analysis · fault reproduction
```


### Talks

Speaking on SIP and real-time media since 2013, mostly at the OpenSIPS Summit
and ClueCon.

| Year | Talk | Venue |
|---|---|---|
| 2026 | OpenSIPS Development with an AI Apprentice: Core Patches, Redis Clustering, and a Rust Module — [recording](https://www.youtube.com/watch?v=1m9vrvvI9fY&t=10626s) | OpenSIPS Summit, Bucharest |
| 2025 | Networking Enhancements to the Dispatcher, MySQL, Redis & rtpengine modules — [slides](https://www.opensips.org/events/Summit-2025Amsterdam/assets/presentations/OpenSIPS_Summit_2025_Norman_Brandinger_Networking_Enhacements_for_3_6.pdf) | OpenSIPS Summit, Amsterdam |
| 2024 | Foundations of building a highly available OpenSIPS / rtpengine system — [slides](https://opensips.org/events/Summit-2024Valencia/assets/presentations/OpenSIPS_Summit_2024_Norman_Brandinger_Highly_Available_OpenSIPS_RTPEengine_System.pdf) | OpenSIPS Summit, Valencia |
| 2023 | An experimental module written in Rust — [slides](https://www.opensips.org/events/Summit-2023Houston/assets/presentations/OpenSIPS_Summit_2023_Norman_Brandinger_An_experimental_module_written_in_Rust.pdf) | OpenSIPS Summit, Houston |
| 2021 | How OpenSIPS solved a tricky SIPREC problem — [recording](https://www.youtube.com/watch?v=JZ1hFDWlcFs&t=7642s) · [slides](talks/2021-siprec/slides.md) · [writeup](talks/2021-siprec/article.md) | OpenSIPS Summit, Distributed |
| 2020 | [mod_mosquitto](https://github.com/freeswitch/mod_mosquitto) — building a FreeSWITCH event_handler module | ClueCon |
| 2018 | Mid-registrar and registration redirection — [slides](https://opensips.org/events/Summit-2018Amsterdam/assets/presentations/OpenSIPS%20Summit%202018%20-%20Norman%20Brandinger%20-%20Using%20the%20mid_registrar%20module%20along%20with%20registration%20redirection.pdf) | OpenSIPS Summit, Amsterdam |
| 2014 | Advanced SIP routing with FreeSWITCH modules | ClueCon |
| 2014 | Advanced SIP routing with OpenSIPS modules — [slides](https://opensips.org/pub/events/2014-08-04_OpenSIPS-Summit_Chicago/Norman_Brandinger-OpenSIPS_Summit_2014-Advanced_SIP_Routing_with_OpenSIPS_modules.pdf) | OpenSIPS Summit, Chicago |
| 2013 | High availability with OpenSIPS — [slides](https://opensips.org/pub/events/2013-08-05_OpenSIPS-Summit_Chicago/Norman_Brandinger-HA_with_OpenSIPS.pdf) | OpenSIPS Summit, Chicago |

Technical reviewer for **FreeSWITCH 1.2** (Packt Publishing, second edition, May 2013, ISBN 978-1-78216-100-4).

### Shipped upstream

Features and fixes that landed in other people's projects, oldest first.

| When | What |
|---|---|
| 2006 | **[The OpenSIPS PostgreSQL driver](https://github.com/OpenSIPS/opensips/commit/2d80fcf1cfed82680a016fe723da03a303f73aff)** — rewrote `db_postgres` in the OpenSER days, adding connection pooling and fetch support. 58 commits to the module between 2006 and 2021, third by commit count ([module docs](https://docs.opensips.org/manual/3-6/modules/db_postgres/)). |
| 2008–2009 | **[FreeRADIUS patches for CDRTool](https://github.com/AGProjects/cdrtool/tree/master/contrib/freeradius-brandinger)** — FreeRADIUS could not account for failed SIP sessions. Five patches adding acct type Failed (15) and MySQL stored-procedure support, carried in AG Projects' CDRTool as `contrib/freeradius-brandinger/` and referenced from its install guide. |
| 2019 | **[mod_mosquitto](https://github.com/freeswitch/mod_mosquitto)** — FreeSWITCH event handler bridging FreeSWITCH events to an MQTT broker. Written from scratch; now maintained upstream under the FreeSWITCH org. |
| 2021 | **[TLS for PostgreSQL in OpenSIPS](https://github.com/OpenSIPS/opensips/pull/2644)** — `db_postgres` `use_tls`, letting any OpenSIPS module reach Postgres over TLS via a `tls_mgm` client domain. |
| 2024 | Reported **[asterisk/asterisk#651](https://github.com/asterisk/asterisk/issues/651)** — MySQL 8.3 turned `qualify` into a reserved word, breaking Asterisk's alembic table scripts; fixed upstream. |
| 2024–2025 | **Networking enhancements across four OpenSIPS modules** — [dispatcher `ping_sock` partition parameter](https://github.com/OpenSIPS/opensips/pull/3527), [MySQL Unix-socket connections](https://github.com/OpenSIPS/opensips/pull/3565), [Redis MOVED redirection](https://github.com/OpenSIPS/opensips/pull/3639), and [per-socket rtpengine command routing](https://github.com/OpenSIPS/opensips/pull/3617). |
| 2026 | **Kamailio fixes** — [tm transaction leak on drop](https://github.com/kamailio/kamailio/pull/4644), [dialog race in `link_dlg_profile`](https://github.com/kamailio/kamailio/pull/4591), [swapped comparison in core atomics](https://github.com/kamailio/kamailio/pull/4638), and a [NULL deref in rtpengine DTMF handling](https://github.com/kamailio/kamailio/pull/4637). |
| 2026 | **[Per-key TTL in the NATS C client](https://github.com/nats-io/nats.c/pull/1000)** — brought `nats.c` KV to parity with nats.go's per-key TTL and limit markers, plus a [follow-up](https://github.com/nats-io/nats.c/pull/1001) preserving the create-path error through the marker-aware retry. |

### Contact

- **[sipnab.com](https://sipnab.com)** — project site
- **[n.brandinger@gmail.com](mailto:n.brandinger@gmail.com)**
- **[linkedin.com/in/nbrandinger](https://www.linkedin.com/in/nbrandinger/)**
- Bugs and feature requests are best filed as issues on the relevant repository
