# dashboard-weight-monitor

Single-file HTML dashboard that combines skinfold caliper (adipometer) and bioelectrical impedance analysis (BIA) data to estimate body fat percentage using 2C, 3C, and 4C compartment models.

What it does

Multi-model body fat estimation: Siri 2-compartment (skinfolds), Lohman 3-compartment (skinfolds + BIA total body water), and Heymsfield 4-compartment (adding bone mineral mass)
ECW/ICW ratio tracking: Calculates extracellular/intracellular water ratio from dual-frequency segmental impedance (20kHz / 100kHz)
Fat distribution mapping: Cross-references subcutaneous fat (skinfold sites) with BIA segmental fat to estimate visceral vs subcutaneous trunk fat
Composite metabolic risk score: Combines waist-hip ratio, visceral fat, body fat %, and ECW/ICW ratio into a single 0-100 index
Fitdays CSV import: Parses the TSV export from the Fitdays app (Multilaser / generic BIA scales), including segmental impedance data
Manual adipometer entry: Jackson-Pollock 7-site equation with automatic density and Siri body fat calculation
Offline-first: All data stored in localStorage, with JSON export/import for backup

Usage
Download body_composition_dashboard.html and open it in any modern browser. No server, no dependencies beyond CDN-loaded Chart.js and Luxon.
Adding data

BIA: Export from Fitdays app → "Importar CSV Fitdays"
Adipometer: Click "+ Adipômetro" and enter the 7 skinfold measurements

The 3C/4C models automatically pair adipometer and BIA entries within a 30-day window.
Background
Consumer BIA scales may use prediction equations applied to the raw impedance data. This dashboard bypasses proprietary equations by using published, peer-reviewed models that combine skinfold-derived body density with BIA-derived total body water, producing estimates that are more accurate than either method alone.

References

Lohman, T.G. (1986). 3-compartment model for body fat estimation
Heymsfield, S.B. et al. (1996). 4-compartment model incorporating total body mineral
Jackson, A.S. & Pollock, M.L. (1978). 7-site skinfold equation for body density
Siri, W.E. (1961). Body density to body fat conversion

