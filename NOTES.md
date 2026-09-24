# Codama homework notes

## Versions used

- `anchor --version`: `anchor-cli 1.1.2`
- `node --version`: `v26.4.0`
- `npx codama --version`: `1.6.3`
- `@codama/renderers-js`: `2.5.0`
- `@solana/kit`: `8.3.0`

## Account resolution

In `contribute`, `fundraiser` still has to be passed because its PDA seed reads `fundraiser.maker` from the account itself; `vault` also has to be passed because its ATA seeds read `fundraiser.mint_to_raise` from that state. Codama can derive `contributorAccount` from the supplied fundraiser and contributor, and `contributorAta` from the supplied mint and contributor. In `initialize`, the fundraiser can be derived because `maker` is an explicit instruction account.
