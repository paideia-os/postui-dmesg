# postui-dmesg — status

**Wave:** postui v1 reference apps
**Current milestone:** none landed — not started
**Version:** unreleased

See [`paideia-os/postui`'s `docs/design.md`](https://github.com/paideia-os/postui/blob/main/docs/design.md)
§3.3 and §5.4 for the full spec and milestone/issue breakdown.

## Milestones

| Milestone | Scope | Status |
|---|---|---|
| M1 | Scaffold + `KIND_DMESG` poll | open, not started |
| M2 | List render (log line buffer, auto-scroll) + TextInput filter | open, not started |
| M3 | Tabs severity split + live tail | open, not started |
| M4 | `DmesgLineView@0.1` semantic-pipe emission + release | open, not started |

## Dependencies

- `paideia-os/postui` M1 (Frame/Terminal loop, Block) before this repo's
  M1 can render anything.
- `paideia-os/postui` M2 (List, Tabs) and M4 (TextInput) before this
  repo's M2/M3.
- `paideia-os/postui` M5 (semantic-pipe conformance) before this repo's M4.

## License

MIT — see LICENSE.
