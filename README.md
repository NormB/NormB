<div align="center">

# Norm Brandinger

**SIP and real-time media infrastructure — in Rust and C**

<a href="https://github.com/OpenSIPS/opensips/pulls?q=is%3Apr+author%3ANormB+is%3Amerged"><img alt="OpenSIPS" src="https://img.shields.io/badge/OpenSIPS-1a5f7a?style=flat-square"></a>
<a href="https://github.com/kamailio/kamailio/pulls?q=is%3Apr+author%3ANormB+is%3Amerged"><img alt="Kamailio" src="https://img.shields.io/badge/Kamailio-2b6cb0?style=flat-square"></a>
<img alt="rtpengine" src="https://img.shields.io/badge/rtpengine-3c6e57?style=flat-square">
<img alt="Rust" src="https://img.shields.io/badge/Rust-b7410e?style=flat-square&logo=rust&logoColor=white">
<img alt="C" src="https://img.shields.io/badge/C-4b5563?style=flat-square&logo=c&logoColor=white">

</div>

I build and debug the parts of telephony that carry actual calls: SIP proxies,
media relays, and the tooling around them. Most of my work is on **OpenSIPS**,
**Kamailio**, **rtpengine** and **FreeSWITCH** — upstream where it belongs, and
in my own tools where nothing suitable existed.

---

### Building

| Project | | |
|---|---|---|
| **[sipnab](https://github.com/NormB/sipnab)** · [sipnab.com](https://sipnab.com) | SIP & RTP capture, analysis and security. One binary, one dependency (libpcap). | [![stars](https://img.shields.io/github/stars/NormB/sipnab?style=flat-square&label=%E2%98%85&labelColor=1c1917&color=0b7285)](https://github.com/NormB/sipnab/stargazers) [![release](https://img.shields.io/github/v/release/NormB/sipnab?style=flat-square&labelColor=1c1917&color=555)](https://github.com/NormB/sipnab/releases) |
| **[opensips-lsp](https://github.com/NormB/opensips-lsp)** | Language server for OpenSIPS routing scripts — completion, diagnostics, go-to-definition. | [![stars](https://img.shields.io/github/stars/NormB/opensips-lsp?style=flat-square&label=%E2%98%85&labelColor=1c1917&color=0b7285)](https://github.com/NormB/opensips-lsp/stargazers) |
| **[kamailio-lsp](https://github.com/NormB/kamailio-lsp)** | The same, for Kamailio configuration files. | [![stars](https://img.shields.io/github/stars/NormB/kamailio-lsp?style=flat-square&label=%E2%98%85&labelColor=1c1917&color=0b7285)](https://github.com/NormB/kamailio-lsp/stargazers) |
| **[devstack-core](https://github.com/NormB/devstack-core)** | Local VoIP development infrastructure — Docker, Postgres, MongoDB, RabbitMQ, Prometheus, Grafana. | [![stars](https://img.shields.io/github/stars/NormB/devstack-core?style=flat-square&label=%E2%98%85&labelColor=1c1917&color=0b7285)](https://github.com/NormB/devstack-core/stargazers) |
| **[voip-stack](https://github.com/NormB/voip-stack)** | Production-shaped OpenSIPS + Asterisk + rtpengine deployment. | [![stars](https://img.shields.io/github/stars/NormB/voip-stack?style=flat-square&label=%E2%98%85&labelColor=1c1917&color=0b7285)](https://github.com/NormB/voip-stack/stargazers) |
| **[homebrew-tap](https://github.com/NormB/homebrew-tap)** | `brew install NormB/tap/sipnab` | |

### Upstream

Merged pull requests. Every count links to the search that produces it.

| Project | Merged |
|---|---|
| [OpenSIPS/opensips](https://github.com/OpenSIPS/opensips/pulls?q=is%3Apr+author%3ANormB+is%3Amerged) | **45** |
| [freeswitch/mod_mosquitto](https://github.com/freeswitch/mod_mosquitto/pulls?q=is%3Apr+author%3ANormB+is%3Amerged) | **5** |
| [kamailio/kamailio](https://github.com/kamailio/kamailio/pulls?q=is%3Apr+author%3ANormB+is%3Amerged) | **4** |
| [signalwire/freeswitch](https://github.com/signalwire/freeswitch/pulls?q=is%3Apr+author%3ANormB+is%3Amerged) | **4** |
| [nats-io/nats.c](https://github.com/nats-io/nats.c/pulls?q=is%3Apr+author%3ANormB+is%3Amerged) | **2** |
| [Vonage/h2o-opensips](https://github.com/Vonage/h2o-opensips/pulls?q=is%3Apr+author%3ANormB+is%3Amerged) | **2** |
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

Speaking on SIP and real-time media since 2014, mostly at the OpenSIPS Summit
and ClueCon.

| Year | Talk | Venue |
|---|---|---|
| 2026 | OpenSIPS Development with an AI Apprentice: Core Patches, Redis Clustering, and a Rust Module — [recording](https://www.youtube.com/watch?v=1m9vrvvI9fY&t=10626s) | OpenSIPS Summit, Bucharest |
| 2025 | Networking Enhancements to the Dispatcher, MySQL, Redis & rtpengine modules | OpenSIPS Summit |
| 2024 | Foundations of building a highly available OpenSIPS / rtpengine system | OpenSIPS Summit, Valencia |
| 2023 | An experimental module written in Rust — [slides](https://www.opensips.org/events/Summit-2023Houston/assets/presentations/OpenSIPS_Summit_2023_Norman_Brandinger_An_experimental_module_written_in_Rust.pdf) | OpenSIPS Summit, Houston |
| 2021 | How OpenSIPS solved a tricky SIPREC problem | OpenSIPS Distributed Summit |
| 2020 | mod_mosquitto — building a FreeSWITCH event_handler module | ClueCon |
| 2018 | Mid-registrar and registration redirection | OpenSIPS Summit |
| 2017 | OpenSIPS & Vonage — A Great Call | OpenSIPS Summit |
| 2014 | Advanced SIP routing with FreeSWITCH modules | ClueCon |
| 2014 | Advanced SIP routing with OpenSIPS modules | OpenSIPS Summit |

### Shipped upstream

- **[mod_mosquitto](https://github.com/freeswitch/mod_mosquitto)** — FreeSWITCH event handler
  bridging FreeSWITCH events to an MQTT broker. Written from scratch; now maintained
  upstream as its own repository.
- **TLS for PostgreSQL in OpenSIPS** — `db_postgres` `use_tls`, letting any OpenSIPS
  module reach Postgres over TLS via a `tls_mgm` client domain.
- **Networking enhancements** across the `dispatcher`, `db_mysql`, `cachedb_redis`
  and `rtpengine` modules.

### Contact

- **[sipnab.com](https://sipnab.com)** — project site
- **[n.brandinger@gmail.com](mailto:n.brandinger@gmail.com)**
- Bugs and feature requests are best filed as issues on the relevant repository
