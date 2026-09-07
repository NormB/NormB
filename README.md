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

Language mix across repositories I own — forks excluded, so it reflects
code I actually wrote:

```
Rust        ████████████████████████████······  82.4%
Shell       ███·······························   8.0%
Python      ██································   4.5%
C           █·································   1.4%
JavaScript  █·································   1.3%
HTML        █·································   0.7%
```

### Contact

- **[sipnab.com](https://sipnab.com)** — project site
- **[n.brandinger@gmail.com](mailto:n.brandinger@gmail.com)**
- Bugs and feature requests are best filed as issues on the relevant repository
