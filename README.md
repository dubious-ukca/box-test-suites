# box-test-suites
A repository for holding UKCA box model test suites

## Tiers

Suites are grouped into three tiers, one folder each. Each tier holds one
folder per suite.

| Folder | When it runs |
| --- | --- |
| `core/` | Pre-commit. Short runs that finish in seconds |
| `main/` | On every pull request |
| `extras/` | Not run in CI, but still valid suites |

## Naming convention

Suite folders are named

```
<chemistry>_<aerosol>_<environment>[_<variant>]
```

- All lowercase. Underscores separate the parts; hyphens are only used
  inside a part.
- `chemistry` is the UKCA chemistry scheme (`i_ukca_chem`):

  | Name | `i_ukca_chem` | Scheme |
  | --- | --- | --- |
  | `trop` | 11 | Standard tropospheric |
  | `raq` | 13 | Regional air quality |
  | `offox-be` | 14 | Offline oxidants (B-E) |
  | `tropisop` | 50 | Trop-isoprene |
  | `strattrop` | 51 | Strat-trop (CheST) |
  | `strat` | 52 | Standard stratospheric |
  | `offox` | 54 | Offline oxidants (N-R) |
  | `cristrat` | 59 | CRI strat |

- `aerosol` is `glomap` (GLOMAP-mode on, `l_ukca_mode`) or `noaero`.
- `environment` is where the box sits, for example `sfc`, `trop`, `strat`
  or `urban`.
- `variant` is optional and names what makes the suite differ from the base
  suite, for example `4step` (a shortened run), `fastjx` or `sp` (single
  precision).

Names do not include the tier, a version, a date or a compiler, so a suite
keeps its name if it moves between tiers. Names are unique across all
three tiers.

Example: `main/strattrop_glomap_sfc` is the 7-day surface run with
strat-trop chemistry and GLOMAP-mode aerosol, and
`core/strattrop_glomap_sfc_4step` is the same suite cut to 4 timesteps.

## Suite READMEs

Every tier folder and every suite folder has a short `README.md`. A suite's
README says what the suite tests and names the old-box Rose suite it
reproduces, if there is one, with how closely it matches (for example
bit-for-bit over steps 0 to 24). Each tier README lists its suites in a
table.
