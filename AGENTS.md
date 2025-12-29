# AGENTS

This file provides project-specific guidance for Codex agents working in this repository. It applies to the entire repo unless overridden by nested `AGENTS.md` files.

## Workflow
- Prefer `rg` for code search instead of recursive `ls`/`grep`.
- Keep Solidity changes formatted with `forge fmt`; the Foundry config enforces a 100-character line length.
- When touching Solidity or Foundry test files, run `forge test` (and add `--match-contract` or `--match-path` for scoped runs when appropriate).
- For EVM-variant checks, consider `forge test --profile post_cancun` or the other profiles in `foundry.toml` if your changes are protocol-sensitive.
- Keep new instructions localized: add nested `AGENTS.md` files when a subdirectory needs extra guidance.

## Notes
- Contracts live in `src/`; Foundry tests live in `test/` and `ext/`.
- JavaScript helpers reside in `js/`. There are no NPM scripts defined; Foundry commands are the primary test surface.
