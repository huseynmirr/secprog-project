# pwman — secure command-line password manager

A CLI password manager that stores entries in a single encrypted vault file,
unlocked by one master password. Built for the Secure Programming course
(ICS0022), Checkpoint 1.

See [DESIGN.md](./DESIGN.md) for the full architecture, threat model, and
cryptographic design decisions.

## Scope

- `pwman init` — create a new vault and set the master password
- `pwman add <name>` — add an entry (username, password, notes)
- `pwman get <name>` — decrypt the vault and print one entry
- `pwman list` — list entry names (vault must be unlocked)
- `pwman remove <name>` — delete an entry
- `pwman passwd` — change the master password and re-encrypt the vault

## Build

Requires: `gcc`, `libsodium-dev`, `make`.

```bash
sudo apt install libsodium-dev   # or your distro's equivalent
make
```

## Run

```bash
./pwman init
./pwman add github
./pwman list
./pwman get github
```

## Status

Checkpoint 1: architecture and threat model complete (see DESIGN.md).
Implementation not yet started.
