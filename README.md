# Grid Impact Statistics

Statistical analyses for the **ElectriGrid** capstone project, which links California distribution grid hosting capacity to household-level demographic data to assess equitable access to distributed energy resources (DERs).

## Overview

This repository extends [Brockway et al. (2021)](https://doi.org/10.1038/s41560-021-00887-6) by replacing circuit-polygon-level household allocation with **direct building-to-line joins**, enabling more granular per-household hosting capacity estimates statewide across SCE, PG&E, and SDG&E service territories.

## Methodology

Brockway et al. allocated hosting capacity to households by weighting circuit polygon values using the share of households within each polygon. We instead spatially join individual building footprints directly to their nearest distribution line segment, then inherit that segment's ICA (Integration Capacity Analysis) hosting capacity values. This avoids the polygon-level aggregation that can mask within-polygon variation.

Hosting capacity types analyzed (following ICA definitions):
- **PV** – solar generation without operational flexibility constraints
- **PV w/ OpFlex** – solar generation with reverse power flow restrictions
- **Load** – new load capacity (EVs, heat pumps, etc.)

## Analyses



## References

Brockway, A. M., Conde, J., & Callaway, D. (2021). Inequitable access to distributed energy resources due to grid infrastructure limits in California. *Nature Energy*, 6, 892–903.
