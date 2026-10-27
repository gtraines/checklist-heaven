# A-10A — Discrepancy Report (Pending Approval)

**Status:** Research complete. Awaiting user approval before applying fixes.

## Reference
`A-10A Flight Manual EN.pdf` — DCS Flaming Cliffs 3 game manual by Eagle Dynamics (104 pp.)

> ⚠️ This is a DCS game manual, not the real T.O. 1A-10A-1. Performance/limitation data (weights, V-speeds, EGT limits, G-limits, crosswind limits) could NOT be verified — the manual simply doesn't contain them.

## Discrepancies — Awaiting Fix Approval

| # | Section | Checklist Value | Manual Says | Fix Proposed | Status |
|---|---------|----------------|-------------|--------------|--------|
| 1 | Operating Limitations — Vfe (Flap Limit) | `200 KIAS` flat limit | `185–219 KIAS` altitude-dependent | Keep 200 KIAS; add note that DCS model enforces altitude-dependent limit | ⏳ PENDING |
| 2 | Weapons — AGM-65D range | `6–8 NM` | `"approaching 6 nm"` (p.58) | Correct to `~6 NM max`; note G variant range unverified | ⏳ PENDING |
| 3 | Weapons — GAU-8/A range | `open fire at 1,200–1,500 m` | Effective below `800 m` (p.93) | Add note distinguishing dive-entry range from effective lethal range | ⏳ PENDING |
| 4 | Operating Limitations — Oil Pressure Min | `15 PSI min → ENGINE SHUTDOWN` | Warning at `27.5 units` (unit ambiguous) | Flag as unverified; cannot resolve unit ambiguity from this reference | ⏳ PENDING |

## Unverifiable from This Reference
The following values appear in the checklist but have no data in the available DCS game manual:
- MTOW, Max Landing Weight
- G-limits (+7.33/−3.0 clean; +5.86 loaded)
- V-speeds (Vr, V2, Vmca, Vref by weight class)
- EGT limits (725°C start / 650°C continuous / 690°C transient)
- N2 max (100%)
- Crosswind limits (25 kts demonstrated / 15 kts wet)
- Pattern altitudes (1,500 ft AGL) and all pattern speeds
- Best glide speed (200 KIAS) and glide range estimates

To verify these, the real T.O. 1A-10A-1 or AFMAN 11-2A-10C Vol 3 would be required.
