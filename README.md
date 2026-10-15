# paramo-thesis-summary

Summary of a thesis on the relationship between evolutionary divergence and historical connectivity in the northern Andean páramos during the Pleistocene, using the Espeletiinae subtribe as the biological model.

## What the thesis asks

Three processes shape divergence during speciation: gene flow, selection, and genetic drift. Gene flow and drift depend heavily on how habitat is spatially configured. The páramo is an unusually clean case to study this because it is an obligately high-elevation ecosystem whose extent changed dramatically with Pleistocene climate: fragments merged and separated repeatedly over roughly 2 million years.

The thesis asks whether this historical connectivity between páramo fragments is detectable in the evolutionary distances between the lineages that live there.

## What is in this repository

- `index.Rmd` — the full narrative summary, rendered as an HTML site. It covers the methodology end to end: paleoclimatic reconstruction of páramo boundaries, movement-cost rasters built from a DEM, connectivity metrics (least-cost distance and current flow) computed in Graphab, a historical-connectivity algorithm that weights those metrics by the duration of each configuration across the phylogeny, and a Generalized Dissimilarity Model (GDM) relating historical connectivity to evolutionary divergence.
- `_site.yml`, `about.Rmd`, `Summary.Rproj` — site scaffolding.
- Rendered site: https://innerhaze.github.io/paramo-thesis-summary/

Each methodological section in the write-up links to the specific repository that holds the code for that step:

- Cost raster: [dem-reclass-paramo](https://github.com/innerhaze/dem-reclass-paramo)
- Connectivity metrics via Graphab + R: [graphab-r-java-automation](https://github.com/innerhaze/graphab-r-java-automation)
- Historical-connectivity algorithm: [paramo-connectivity-algorithm](https://github.com/innerhaze/paramo-connectivity-algorithm)
- GDM analysis: [gdm-connectivity-paramo](https://github.com/innerhaze/gdm-connectivity-paramo)

## Main result

Historical connectivity is a significant explanatory variable for evolutionary distances when occurrence patches are far apart. When patches are close together, Euclidean distance explains divergence better. The study is a first attempt to quantify how páramo spatial configuration over time has influenced the diversification of Espeletiinae.

## Known limitations

- Species occurrence data are present-day. Connectivity between lineages at older time points is computed using current patches, which may not be where the lineage lived at the time.
- When several species occupy the same patch, Graphab treats the patch as a single unit, which complicates species-pair measurements inside dense regions.
- Phylogenies cannot be analysed deeper than ~2.2 million years, the maximum covered by the paleoclimatic model used.

## References

- Diazgranados, M., & Barber, J. C. (2017). The endemic Espeletia complex: Phylogenetics, morphological evolution, and biogeography of the most diverse plant clade in the high Andes. *Frontiers in Plant Science, 8*, 2058.
- Pouchon, C., et al. (2021). Phylogenetic signatures of ecological divergence and leapfrog adaptive radiation in Espeletia. *American Journal of Botany, 108*(1), 113–128.
- Flantua, S. G. A., O'Dea, A., Onstein, R. E., Hooghiemstra, H., & Hoorn, C. (2019). The flickering connectivity system of the north Andean páramos. *Journal of Biogeography, 46*(8), 1808–1825.
