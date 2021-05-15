# cluster-gas-analysis
This is an exploratory analysis of plasmic matter found in the galaxy clusters of the [IllustrisTNG Simulations](https://www.tng-project.org)- TNG100.
This work was performed as part of my summer research with Simons Observatory as an NSBP scholar. 


## Background
Galaxies, groups of stars and dust, are often tugged by dark matter halos into even larger groups. These groups are called galaxy clusters and to the suprise of many their excessive (baryonic) mass comes not from stars or planets but from a permeative gas called the intracluster medium. In fact there is 10 times more mass in the gas than in all the stars and planets. In my research, I am seeking to explore and visualize characteristics of this gas.

## Contents
### analyze_gas_data
This notebook conatains an analysis of Gas data from the 9 most massive halos of the TNG simulation. Preprocessing of this data is done by Sam Goldstein, who filtered the set to include only the most massive halos(clusters), on account of their reliability. Using Matplotlib.hist2D I plot each of the halos position, density and tempurature distributions. These parameters are of major concern in the growing studies of the Sunyaev-Zeldovich effect and Dark matter research.
Finally, **Temperature vs Density plots were produced and found to vary quite widley** among the sample population.

While gas tempurature is not part of the dataset it ws solved using the following equations:

> mean_mol_weight = 4*mp  / (1 + 3*x_h + 4*x_h*gas_e_abundance) 

> gas_temp = (gamma - 1) * (gas_u/kb) * mean_mol_weight * ratio_EM

### cluster_gas_analysis- Density vs Temperature 
The high variance in the density-temperature relationship was unexpected to me so I decided to compare a larger sample. To better understand the trend, a large sampleset from over 700 distinct halos was compiled. A challenge arised in choosing which halos to sample. To solve this problem, two analysis were run: one for low-mass clusters on the range: (1E10.5M☉/h - 1E11M☉/h) and another for high-mass clusters on the range: (1.28e+12M☉/h - 5.83e+14M☉/h). Low mass clusters were found to be difficult to work with. Each halo contains up to thousands of particles. Yet in low-mass halos, this was not always the case. To ensure that each low-mass halo contributed an adequate number of particles, an algorithm was applied to search for good halo candidates. 

### Results
From the plots it is evident that the low-mass and high-mass halos exhibit very different density-temperature relationships. This indiactes that halo mass or its implicated factors play a large role in the distribution of these clusters. If I has more time I would like to filter the halos according to the standard deviation of their tempuratures. I think this would exclude many anomalies and better expose the underlying relationships.

## Credits
Many thanks to the team: Sam Goldstein, and Bhuvnesh Jain from UPenn for their direction in this project and exposing me to Illustris. Sam was a huge help in downloading and processing the data. I am grateful for the opportunity and experience.
Thanks to Professor Kasey Wagoner from the Univerity of Princeton for all his support in the program as well.


NSBP and Simons Observatory Were wonderful for allowing me to work with them on this project. Many thanks to all!
