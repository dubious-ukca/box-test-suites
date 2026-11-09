# strattrop_glomap_sfc

Strat-trop chemistry (`i_ukca_chem=51`) with GLOMAP-mode aerosol, in a
surface box (30°N, 1000 hPa, 288.15 K). Offline photolysis rates. 7 days of
1-hour steps (168 steps).

A copy of `examples/default` in `ukca-box-model`.

## Old-box equivalent

**Rose suite `u-ed364`** (the master reference): `nml_box_sfc`,
`chem_tracer_pars_STwGMaero`, `djrat_0lat_12z_969hPa_v2.txt`. `u-ed364` runs
24 steps, so only steps 0 to 24 can be compared.

Bit-for-bit identical to `u-ed364` over steps 0 to 24, except for the H2O
tracer (the old box keeps H2O in q). Checked 2026-11-06.
