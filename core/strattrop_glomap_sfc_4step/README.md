# strattrop_glomap_sfc_4step

Strat-trop chemistry (`i_ukca_chem=51`) with GLOMAP-mode aerosol, in a
surface box (30°N, 1000 hPa, 288.15 K). Offline photolysis rates. Four
1-hour steps.

The same as [`main/strattrop_glomap_sfc`](../../main/strattrop_glomap_sfc/),
cut to 4 steps (`model_duration=14400`).

## Old-box equivalent

**Rose suite `u-ee345`** (a copy of `u-ed364` with `run_target_end` set to 4
hours): `nml_box_sfc`, `chem_tracer_pars_STwGMaero`,
`djrat_0lat_12z_969hPa_v2.txt`.

Bit-for-bit identical to the old box at every step (0 to 4), except for the
H2O tracer. The old box keeps H2O in q, so its H2O tracer column is not
comparable. Checked 2026-11-06 against `u-ed364` (`tracer_out.hex`) and
`u-ed365` run3 (UKCA dump). Ignore `eta_theta_levels` and
`ukca_config:l_ukca_h2o_feedback` in the dump comparison (known
differences).
