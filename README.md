# EIP-8268 Devnet

Kurtosis devnet configuration for testing EIP-8268 block access list behavior across Geth, Reth, and Lodestar.

## What It Runs

- Execution clients: Geth and Reth
- Consensus clients: Lodestar
- Additional services: Dora, tx-fuzz, Spamoor
- Snooper: enabled for engine/RPC traffic inspection

## Fork Schedule

The included configs use a fast local schedule:

```yaml
fulu_fork_epoch: 0
gloas_fork_epoch: 1
heze_fork_epoch: 2
seconds_per_slot: 6
```

With 32 slots per epoch, Heze starts at slot 64.

## Run

Use local images/config:

```sh
make run
```

Use registry images/config:

```sh
make run-registry
```

Stop and remove the enclave:

```sh
make stop
```

The enclave name is `bals`.

## Logs

Temporary log captures for HackMD notes can be stored in:

```text
hackmd-logs/
```

That folder is ignored by git.

## License

This project is available under either of:

- MIT License, see `LICENSE-MIT`
- Apache License, Version 2.0, see `LICENSE-APACHE`
