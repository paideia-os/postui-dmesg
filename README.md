# postui-dmesg

paideia-os klog tail with filter — a `postui` reference app proving the
library across a `List` + `TextInput` + `Tabs` widget mix.

## Status

**Design phase — not started.** Depends on `paideia-os/postui` M1
(skeleton), M2 (List/Tabs), and M4 (TextInput) landing first. See the
authoritative design at [`paideia-os/postui`'s `docs/design.md`](https://github.com/paideia-os/postui/blob/main/docs/design.md)
§3.3 for widget mix, data source, semantic records, and milestone
breakdown; see `STATUS.md` here for the rollup.

## Data source

`KIND_TUI_CANVAS`'s sibling kernel facility, `KIND_DMESG`
(`src/kernel/core/cap/kind_dmesg.pdx` in `paideia-os/paideia-os`),
polled/subscribed for new lines.

## License

MIT — see LICENSE.
