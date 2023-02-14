# Lookup and Modelling Proposed Westminster Parliamentary Constituency Boundaries

This repo contains two files:

### Lookup of Output Area (2011) to LSOA (2011) to MSOA (2011) to Ward (Feb 2021) to Westminster Parliamentary Constituency (2010) to Revised Westminster Parliamentary Constituency (2022) to Local Authority (Feb 2021)
* [oa_lookup.csv](https://github.com/owenwntr/proposed_constituency_boundaries/blob/main/oa_lookup.csv)
* Rough lookup made using published shapefiles of proposed boundaries from the Boundary Commissions of England, Wales and Scotland, combined with population weighted centroids of 2011 Output Areas

### Constituency Voting Estimates 2019 Election
* [estimates.csv](https://github.com/owenwntr/proposed_constituency_boundaries/blob/main/estimates.csv)
* Estimates of 2019 Election vote share by party for new constituencies, using a rough interpolation method
* Models of each party's vote share are made using constituency-level census data, then this model is applied to the intersection of old and new constituencies, before being scaled to match the true results. These estimates are then re-aggregated for the new boundaries.
* This method likely performs poorly for small parties (especially the Greens, for which the regression model performs poorly) but gives a good sense of the overall Lab-Con picture
