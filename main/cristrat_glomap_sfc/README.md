# cristrat_glomap_sfc

CRI-Strat chemistry (`i_ukca_chem=59`) with GLOMAP-mode aerosol, in a
surface box (30°N, 1000 hPa, 288.15 K). Offline photolysis rates. 7 days of
1-hour steps.

A copy of [`strattrop_glomap_sfc`](../strattrop_glomap_sfc/) with only
`i_ukca_chem` changed. The tracer, NTP and photolysis inputs are still the
strat-trop ones, so it tests that CRI-Strat runs, not that its results are
realistic:

- 172 of 208 tracers and 52 NTPs start at the 1e-15 default.
- CRI photolysis rates not in `jrate.txt` are zero: `jforma`, `jformb`,
  `jprpal`, `jmacr2`, `jcb3a`, `jcb3b`, `jcb3c`, `jcs2`, `jcos`, `jh2so4`,
  `jso3`. So HCHO is not photolysed.

## Old-box equivalent

None. The old-box Rose configurations (`u-dr407`) have no CRI-Strat setup.
