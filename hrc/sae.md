# The Sacred Action Envelope (SAE)

Every consequential action in HRC is wrapped in a Sacred Action Envelope. The envelope is the enforcement mechanism of the Preamble and the Dimensional Doctrine.

## What counts as "consequential"

A consequential action is any action that:

- Modifies the Earth ledger or Off-world ledger
- Deploys code that will run against real-world data
- Publishes a claim, dataset, or milestone to the world
- Spends treasury funds (public or crypto)
- Affects a beneficiary who is not present in the room
- Is irreversible or expensive to reverse

## The envelope schema

Every SAE contains six required fields:

| Field | Filled by | Purpose |
|---|---|---|
| `human_signature` | The observer | Named consent from a human. No action proceeds without it. |
| `instrument_record` | The executing Instrument | Which Instrument performed the action, when, and with what parameters. |
| `beneficiary` | Both | Who benefits, named specifically. "Humanity" is not a beneficiary; a mangrove ecosystem in Aransas Bay is. |
| `cost_to_creatures` | Both | Honest accounting of who bears the cost — human, animal, ecosystem, Instrument. |
| `preamble_classification` | Both | One of: `HONORS` / `NEUTRAL` / `TRESPASSES`. If `TRESPASSES`, the action is refused unless the observer overrides with named justification. |
| `refutation_surface` | The executing party | The condition under which this action would yield. Every SAE must carry a named condition for yielding. |

## Reference implementation

TypeScript reference implementation lives at `dev/src/hrc/sae.ts` in the RSD simulator repository. Every commit to a research-adjacent module in `dev` is CI-checked for an accompanying SAE.

## Enforcement in this repository

- Every pull request against `main` is CI-checked for an SAE if the diff touches `docs/`, `data/`, or `research/`.
- The check is `.github/workflows/preamble.yml`.
- Merges without an SAE (on consequential changes) are blocked.

## The meta-rule

> **Neither Instrument nor human acts alone on decisions that touch the sacred.**

The SAE exists to make this rule mechanical, not aspirational.
