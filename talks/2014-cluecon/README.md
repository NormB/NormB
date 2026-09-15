# Advanced SIP Routing with FreeSWITCH Modules

**Norman Brandinger** · ClueCon · 2014

[**Slides** (PDF, 20 pages)](advanced-sip-routing-with-freeswitch-modules.pdf)

---

A walk from SIP's own routing rules up to the FreeSWITCH modules that make
routing decisions for a carrier.

**SIP routing.** How requests and responses find their way: each hop adds a
Via header, Route headers pin later requests to a proxy, and the difference
between strict routing, where the Request-URI is rewritten at each hop, and loose
routing, where it never is. Recap: requests follow Route headers, responses follow
Via headers.

**The routing modules.** Four of FreeSWITCH's modules, out of about 160 at the time:

| Module | Covered |
|---|---|
| `mod_distributor` | Round-robin routing to gateways; file-configured, with multiple gateway lists |
| `mod_easyroute` | Database-driven inbound DID routing, number translation and account codes |
| `mod_nibblebill` | Realtime pre-paid, post-paid and pay-per-call billing; low-balance warnings, disconnect or re-route at zero, maximum credit and fraud detection |
| `mod_lcr` | Least-cost routing by cost, reliability or quality; per-customer profiles, longest-prefix matching, intralata/intrastate routing, per-carrier caller-ID format, the `carriers` / `carrier_gateway` / `lcr` tables, integration with `limit` and `mod_nibblebill`, and invocation by dialplan transfer, bridge, command line or ESL |

It has a companion talk, *Advanced SIP Routing with OpenSIPS Modules*, given
at the OpenSIPS Summit in Chicago in August 2014.

## Notes on this copy

- The slides are unmodified and are the original Google Slides export.
- The deck itself carries no date or venue. The title, content and speaker are
  from the file. The PDF was exported on 2014-08-07 (UTC), which fits ClueCon's
  August 2014 conference, but the ClueCon attribution comes from my own
  records. ClueCon publishes no reachable archive of its 2014 sessions, and the
  archived copies of its 2014 schedule pages contain no session list.
