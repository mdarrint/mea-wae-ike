# mea-wae-ike

**mea-wae-ike** (Hawaiian: "knowledge weaver/braider") — a knowledge aggregator in the style of the *arr apps (Sonarr, Radarr, etc.) but for knowledge management.

## Language & stack

- **Elixir** (see `.gitignore` for build artifacts: `/_build`, `/deps`, `/cover`)
- GPL-3 licensed

## Project conventions

- Standard Mix project layout expected (`lib/`, `test/`, `config/`, `mix.exs`)
- Config secrets go in `config/*.secret.exs` (gitignored)

## Common commands

```sh
mix deps.get       # install dependencies
mix compile        # compile
mix test           # run tests
mix format         # format code
```

## Notes

- Early-stage project — no source files yet as of initial commit
