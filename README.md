# postui-dmesg

paideia-os klog tail with filter — a `postui` reference app proving the
library across a `List` + `TextInput` + `Tabs` widget mix.

## Status

**v1.0.0 shipped 2026-09-07.** All M1..M4 milestones landed:
- **M1** klog_poll (sys_dmesg sysno 13 consumer, 64-slot log ring)
- **M2** view_list (auto-scroll List adapter)
- **M3** view_filter (TextInput + naive strstr) + view_tabs (5-tab severity split)
- **M4** SemanticEmit DmesgLineView@0.1 via sys_semantic_send (sysno 115)

Depends on `paideia-os/postui` M1-M4 (List, Tabs, TextInput). See
authoritative design at [`paideia-os/postui`'s `docs/design.md`](https://github.com/paideia-os/postui/blob/main/docs/design.md)
§3.3.

## Data source

Live tail of paideia-os kernel log ring via `sys_dmesg` (sysno 13);
future variant will swap to `KIND_DMESG` cap subscribe when TCB
cap-slots land.

## Known follow-ups

- **postui-dmesg#8** — view_tabs severity mapping uses fabricated
  syslog priorities (0=emerg/3=err/4=warn/6=info); paideia-os actually
  uses LEVEL_* (0=PANIC..5=TRACE). Mapping + tab labels need rewrite;
  currently latent because klog_poll M1 stubs severity to 0.
- **paideia-os#2352** — sys_semantic_send (sysno 115) not yet landed
  in paideia-os kernel dispatch; semantic_emit returns -ENOSYS until
  handler lands.

## License

MIT — see LICENSE.
