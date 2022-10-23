# BIOL3207-BIOL6207_Assignment2
Meta-analysis of Ocean Acidification Effects on Behaviour for the paper by Clark et al (2020) https://www.nature.com/articles/s41586-019-1903-y. This study was an experimental study across 5-6 different reef fish that looked at comparing the effect of elevated CO2 (in ppm) relative to some control on fish behaviour.

## Getting Started
### meta-data 
Original Data information: 
"Data, analysis script and associated files for:"            
"Clark TD, Raby GD, Roche DG, Binning SA, Speers-Roesch B, Jutfelt F, Sundin J (in prep) Ocean acidification does not impair the behaviour of coral reef fishes"            
             
"Data collected by TDC, GDR, DGR, SAB, BSR, FJ and JS. Please refer to the manuscript for data collection methods and statistical analyses. For questions or to notify the authors if any errors are identified in the data, please contact Tim Clark (t.clark@deakin.edu.au), Graham Raby (graham.d.raby@gmail.com), and/or Dominique Roche (dominique.roche@mail.mcgill.ca)."    



### directory layout
.
├── src                                                                                           # R script                               
├── data                                                                                          # meta-data files
│       ├── assignment2                                                                     
│                  ├── clark_paper_data.csv                                                       # meta-data for clark paper
│                  ├── meta-data_ocean_meta.csv                                                   # ocean meta data from all paper
│                  ├── OA_activitydat_20190302_BIOL3207.csv                                       # fish activity information from clark paper
│                  └── ocean_meta_data.csv                                                        # ocean analysis data1. 
├── LICENSE
└── README.md

### Statistical Analysis
1. load the data 
2. Correctly calculate the log response ratio (lnRR) effect size using metafor’s escalc() function.
3. meta-analytic model fitted to the data that controls for the sampling variance of lnRR, using metafor’s rma.mv() function.
4. Testing publication bias using Funnel plot, Time-lag plot.
5. Formal meta-regression model to test time-lag bias and file-drawer biases.


