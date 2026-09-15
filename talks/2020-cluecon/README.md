# How to Build a FreeSWITCH event_handler Module

**Norman Brandinger** · ClueCon · 2020

[**Slides** (PDF, 24 pages)](how-to-build-a-freeswitch-event-handler-module.pdf)

---

A walkthrough of building a FreeSWITCH event handler module from scratch. The
ideas come from [mod_mosquitto](https://github.com/freeswitch/mod_mosquitto),
which connects FreeSWITCH to an MQTT broker.

**Background.** What FreeSWITCH events are: asynchronous notifications such as
`HEARTBEAT`, `CHANNEL_CREATE` and `BACKGROUND_JOB` that any internal or external
module can subscribe to. Then what modules are, counted by category (181 at the
time), and why a new one was worth writing. MQTT's publish/subscribe model,
through Mosquitto or RabbitMQ, lets many FreeSWITCH servers and the business logic
behind them stay decoupled.

**The build.** A minimal module grown step by step:

| Slides | Covered |
|---|---|
| Where modules live | `src/mod/{category}`, out-of-tree modules, and pulling them in through `modules.conf` |
| Minimal module | `SWITCH_MODULE_LOAD_FUNCTION`, `SWITCH_MODULE_RUNTIME_FUNCTION`, `SWITCH_MODULE_SHUTDOWN_FUNCTION` and `SWITCH_MODULE_DEFINITION` |
| `Makefile.am`, `mod_example.h` | Build rules, and the event and globals structures: memory pool, API interface, event hash table and mutex |
| `mod_example_load`, `example.conf.xml`, `load_config` | Reading the event list from XML configuration and binding each event with `switch_event_bind_removable` |
| `event_handler` | Serializing each event to JSON with `switch_event_serialize_json` |
| `add_cli_api`, `exec_api_cmd` | Adding an `example status` console command that walks the event hash table under the mutex |
| `mod_example_shutdown` | Unbinding the events and tearing everything down |
| `fs_cli` | A live session: load the module, receive a `HEARTBEAT`, run `example status`, unload |

## Notes on this copy

- The deck names ClueCon 2020 on every slide.
- Converted to PDF from the original PowerPoint. The deck is set in Menlo, which
  is replaced here by DejaVu Sans Mono, the font Menlo is derived from.
- The server's public IPv4 address and hostname in the `fs_cli` output on
  slide 22 have been redacted. Nothing else has been changed.
- The example module repository linked on the last slide,
  `github.com/NormB/mod_example`, is no longer available.
  [mod_mosquitto](https://github.com/freeswitch/mod_mosquitto), the module the
  talk builds toward, is maintained upstream.
