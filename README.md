# BIOL3207-BIOL6207_Assignment2
Meta-analysis of Ocean Acidification Effects on fish's Behaviour.

## Getting Started
### meta-data 
1. ocean_meta_data: Result of Studies for ocean acidification studies on fish behavior. Data is coming from various studies' result from 2009 to 2020.
2. meta-data_ocean_meta: Explaination of all the columns in ocean meta data.
3. clark_paper_data: Information for clark's paper: Ocean acidification does not impair the behaviour of coral reef fishes.
4. OA_activitydat_20190302: the experiment data for clark's study


### directory layout
```
.
├── src                                                                            # R script                               
├── data                                                                           # meta-data files
│       ├── assignment2                                                                     
│                  ├── clark_paper_data.csv                                        # meta-data for clark paper
│                  ├── meta-data_ocean_meta.csv                                    # ocean meta data from all paper
│                  ├── OA_activitydat_20190302_BIOL3207.csv                        # fish activity information from clark paper
│                  └── ocean_meta_data.csv                                         # ocean analysis data1. 
├── LICENSE
└── README.md
```

### Statistical Analysis workflow
1. Generate data for Clark's paper
  1.1. load the data from OA_activitydat_20190302.csv, 
  1.2. generate summary statistics 
  1.3. merge with clark_paper_data.csv
2. Merge the result from step 1 with ocean_meta_data.csv
3. Correctly calculate the log response ratio (lnRR) effect size using metafor’s escalc() function for data from step 2.
4. meta-analytic model fitted to the data from step2 for the sampling variance of lnRR, using metafor’s rma.mv() function with random effect of study and observation. 
5. Testing publication bias using Funnel plot for data from step 2.
6. Using Time-lag plot to test effect sizes changes over time for data from step 2.
7. Formal meta-regression model to test time-lag bias and file-drawer bias for data from step 2.
   7.1. including year as a fixed effect
   7.2. including inverse sampling variance as a fixed effect
