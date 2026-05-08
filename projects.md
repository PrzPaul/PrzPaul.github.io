---
layout: single
classes: wide
title: Projects
permalink: /projects/
author_profile: true
---

## CBRN Alert: Web App for Atmospheric Dispersion Modelling of CBRN releases



Publication:

- Perez, P., Benhassine, M., Quinn, J., Janssens, B., & Van Utterbeeck, F. (2025). Simulation of a nuclear fallout scenario in the Zaporizhzhia nuclear power plant during the Ukraine conflict: Implications of dose rate distributions for downwind populations. *Military Medicine, 190*(Supplement_2), 536–542. [https://doi.org/10.1093/milmed/usaf263](https://doi.org/10.1093/milmed/usaf263)

Software:

- CbrnAlert web application. Source code available on [GitHub](https://github.com/cbrnalert/CbrnAlert).
- [FLEXPART](https://www.flexpart.eu/) dispersion model.
- [flex_extract](https://flexpart.img.univie.ac.at/flexextract/). ECMWF data retrieval and processing software for FLEXPART model input.
- Julia packages (with GitHub links) contributed to: [Flexpart.jl](https://github.com/tcarion/Flexpart.jl), [FlexExtract.jl](https://github.com/tcarion/FlexExtract.jl), [ATP45.jl](https://github.com/tcarion/ATP45.jl).

## Sensitivity analysis of WRF model parameterization on CO<sub>2</sub> column mole fractions

Top-down carbon flux estimates, crucial for accurately monitoring and reducing our greenhouse gas emissions, combine atmospheric concentration measurements and inverse modelling. The goal of this project was to quantify uncertainties in simulated CO<sub>2</sub> column mole fractions due to atmospheric transport errors in the Weather Research and Forecasting (WRF) model, and to evaluate the contribution of different signals (background, biosphere, anthropogenic sources) to these uncertainties. We focused on modelling the city plume of Berlin within a high spatial resolution (2 by 2 km) nested domain over multiple days, using ERA5 reanalysis data, and emissions datasets from TNO and CAMS.

{% include image.html url="/assets/images/wrf-sims.gif" description="Simulated CO<sub>2</sub> concentrations from Berlin's city plume (left) and neighboring power plants (right) using WRF." %}

Results from an ensemble of models with varying physical parameterizations showed that planetary boundary layer (PBL) and land surface model (LSM) schemes produced the largest uncertainties on simulated concentrations. Interestingly, the use of an urban surface scheme didn't impact the results much, even for a large city like Berlin. Furthermore, in this high spatial resolution domain where organized convection is resolved, the uncertainties from cumulus parameterization (CP), needed in the coarser parent domain and which usually has a large effect, seemed to fade across the ensemble by the end of the simulations. Finally, it was also concluded that modelled anthropogenic emissions had a much larger contribution to overall WRF uncertainty than natural CO<sub>2</sub> fluxes.

Internship report:

- Perez, P. (2020). *Quantifying uncertainties in CO<sub>2</sub> column mole fractions due to atmospheric transport errors in the WRF model, over Berlin* [[Internship report](/assets/files/WRF_uncertainties_Paul_Perez.pdf)]. Earth program, SRON.

Software:

- Weather Research and Forecasting (WRF) model available [here](https://www.mmm.ucar.edu/models/wrf).

{% include image.html url="/assets/images/wrf-results.png" description="The table presents how large the variability in CO<sub>2</sub> mole fraction is relative to the mean city plume signal, of 1 ppm. It gives an estimation of WRF uncertainty from the physical parameterization, for every signal, as well as of the contribution of the different signals to the uncertainty. (PBL: Planetary Boundary Layer; LSM: Land Surface Model; CP: Cumulus Parameterization)" %}

## Booming sand dunes on Mars?

Booming sand dunes are one of Nature's phenomena that make you question in awe: Is that really happening? This [video](https://youtu.be/4yFaMsUawi4?si=8ECLsJsEO_ldaQKh) shows an example of "sonic sand", emitting a rich brassy sound between 50 and 400 Hz when sheared locally or during an avalanche on the slipface of a dune. This rather rare type of sediment exhibits particular granulometric, shape and surface characteristics, due to the grains’ erosion and transport history, and produces sounds when enough grains of similar sizes roll over those below in a synchronized manner, creating a vibrating layer like the membrane of a speaker. Establishing the existence of sand acoustic emissions on Mars and recording them using rover microphones could thus become a new form of observable for scientists to estimate from a distance the surface sediment’s characteristics and history, as well as the granular flow dynamics taking place.

In my master's thesis, I explored this idea, trying to evaluate how likely the phenomenon were to exist on Mars, and how the Martian environment would affect if differently than on Earth. After finding many similarities between booming sand grains and Martian dune sand, as well as showing that the muted Martian soundscape would likely allow rovers to detect such low frequency signals from a few tens of meters, I focused on studying the impact of interstitial air pressure within the sand bed on the sound emission mechanism. Two experimental vacuum chamber setups were developed, where both normal and booming sand were set in motion under a range of pressure levels, after which the characteristics of the emitted sounds were measured, processed, validated and analysed.

{% include image.html url="/assets/images/booming-setup.png" description="Sketches of the shaking jar (left) and laboratory avalanche (right) vacuum chamber experiments used to test the booming sand phenomenon at Mars-like pressure levels. Accelerometers were used to account for movement variation during measurements." %}

It was found that at Mars-like pressure levels, the booming sand produced sounds louder and longer than expected. The early phase of the sound, not present at Earth like pressure levels, also had a higher frequency, pointing to a thinner sheared layer being able to produce the desired sound. These preliminary findings suggest that lower pressure levels might enhance the booming sand emission phenomenon with seemingly more sonic sand grains synchronizing and a lowering of the sound emission threshold.

Thesis report:

- Perez, P. (2023). *The impact of interstitial air pressure on sand acoustic emissions in the context of Mars exploration* [Master's thesis, Delft University of Technology]. TU Delft Repository. [https://resolver.tudelft.nl/uuid:318ebd5f-1f23-4e56-9a33-890d80ada65a](https://resolver.tudelft.nl/uuid:318ebd5f-1f23-4e56-9a33-890d80ada65a)

Software:

- [GRADISTATv8](https://www.researchgate.net/publication/277015584_GRADISTATv8). An excel package for grain size distribution and statistics.
- Model for acoustic absorption vs. sound frequency in different planetary environments. Based on [Liu et al. (2017)](https://doi.org/10.1098/rspa.2017.0496). Code available on [GitHub](https://github.com/PrzPaul/Acoustic-Absorption-in-Gas-Mixtures).
- [LabVIEW](https://www.ni.com/en/shop/labview) for all the data acquisition during experiments.

{% include image.html url="/assets/images/booming-results.png" description="Left: Comparison of theoretical and experimental sound pressure levels of booming sand and normal sand, as a function of chamber pressure, in the shaking jar experiment. While the regular sand behaves as predicted, the booming sand's sound becomes louder than expected as the pressure decreases. Right: Comparison of booming sounds at ambient Earth pressure and Mars-like pressure, during the laboratory avalanche experiment. The amplitudes are scaled in order to better compare the shape and length of the acoustic emissions produced. The sound at low pressure begins earlier, at a higher frequency (result not shown here), suggesting that perhaps a thinner sheared layer of sonic sand would be required to emit a sand acoustic emission." %}