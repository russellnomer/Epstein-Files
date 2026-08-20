# Security Policy

## Classification

**Public** GitHub repository (`russellnomer/Epstein-Files`). This document is high-level by design. Do not publish exploit write-ups, scraping recipes against protected systems, or any material that is not already in the public government release.

This repo is a **mirror + index** of U.S. Department of Justice Epstein Files datasets (1–12): official ZIP links, community torrents, Internet Archive mirrors, and hashes. It does not host the bulk archives inside Git.

## Data handled

- Public government-released records and community preservation metadata (URLs, magnet links, SHA256)
- **No** private credentials, accounts, or application sessions
- Dataset contents themselves can include highly sensitive personal information that was released by the DOJ. Inclusion of a name does **not** imply guilt.

Operators and downloaders must:

- Follow [ARCHIVAL_DISCLAIMER.md](ARCHIVAL_DISCLAIMER.md)
- Not use this index for harassment, doxxing, or unlawful redistribution
- Not request, upload, or link **non-public** leaks, hacks, or illicit imagery
- Prefer hash verification (SHA256) before treating a copy as authentic

## Authentication

None. Clone, read, and verify. GitHub issues/PRs use ordinary GitHub accounts.

Related private product: `russellnomer/Epstein-Files-Analyst` (separate security policy).

## Secrets

No application secret manifest. There is no `DATABASE_URL` or API key store in this tree.

If you add automation later (bots, GH Actions), use repository secrets — never commit tokens.

## Attack surface

- Public markdown index (supply-chain: malicious PR that swaps URLs/hashes)
- Magnet links and third-party mirrors (treat as untrusted until hashes match)
- `AnalysisEngine` and any helper scripts run **locally** on the operator’s machine
- Social-engineering via issues (“please add this leak”)

## Findings / defensive notes

1. **Integrity is the control** — prefer SHA256 in this README over “a person sent a ZIP.”
2. **Link substitution** — review PRs that change DOJ URLs, magnets, or hashes with extra care.
3. **Volatile upstream** — DOJ links throttle or vanish; that is an availability issue, not a reason to accept unmarked sources.
4. **Sensitive public data** — downloading the archives may be lawful for preservation; **misuse is not**. Keep discussions sourced and non-speculative.

## Reporting

Report security problems (malicious links, hash mismatches, malware in a claimed mirror) to **help@russellnomerconsulting.com**.

You may also open a GitHub issue for **hash mismatches** and **broken official mirrors**. Do not attach illegal content. Do not paste step-by-step exploit instructions.

Owner: Russell Nomer / Russell Nomer Consulting.
