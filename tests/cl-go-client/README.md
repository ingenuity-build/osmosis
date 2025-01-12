# Concentrated Liquidity Go Client

This Go-client allows connecting to an Osmosis chain via Ignite CLI and
setting up a concentrated liquidity pool with positions.

## General Setup FAQ

- Update constants at the top of the file accordingly.
   * Make sure keyring is set up.
   * Client home is pointing to the right place.

## LocalOsmosis Setup

Make sure that you run `localosmosis` in the background and have keys
added to your keyring with:
```bash
make localnet-keys
```

See `tests/localosmosis` for more info.

## Running

```bash
go run tests/cl-go-client/main.go
```

In the current state, it does the following:
- Queries status of the chain to make sure it's running.
- Queries pool with id 1. If does not exist, creates it
- Sets up one CL position

## TODOs

- Create many positions across multiple accounts with randomized parameters.
