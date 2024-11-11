# Mangrove-vs.-Reef-O2-Regulation
"Increased  capacity for oxyregulation retained in Pocillopora acuta corals transplanted from mangrove lagoons to a reef-flat on the Great Barrier Reef"

Nicole J. Dilernia*1, David J. Suggett1,2, Christine D. Roper1, Rachel Alderdice3, Christian R. Voolstra3, Michael Kühl4, Emma F. Camp1.

1Climate Change Cluster, University of Technology Sydney, Ultimo 2007, NSW, Australia.
2KAUST Coral Restoration Initiative (KCRI) and Red Sea Research Center (RSRC), King Abdullah University of Science and Technology, Thuwal, 23955, Saudi Arabia.
3Department of Biology, University of Konstanz, 78464 Konstanz, Germany
4Department of Biology, Marine Biological Section, University of Copenhagen, Strandpromenaden 5, 3000 Helsingør, Denmark

*Corresponding author: Nicole J. Dilernia, Nicole.J.Dilernia@student.uts.edu.au

**Abstract**
Loss of oxygen (O2) from the world’s oceans continues to negatively impact temperate and tropical coral reefs. Reef-neighbouring extreme ecosystems such as mangrove lagoons that are routinely subjected to low-O2 conditions conventionally considered “hypoxic” may be harbouring corals preconditioned with a higher capacity for oxyregulation, which could be better suited to cope with future-predicted low-O2 seawater conditions. We investigated differences in the hypoxic response of the tropical coral Pocillopora acuta – reciprocally transplanted 1-year prior between Low Isles reef flat (a comparatively more stable environmental system) and Woody Island mangrove lagoon, on the Great Barrier Reef. Analysing coral Hypoxia Response Curves and additional metabolic function and physiology, we exposed the capacity of mangrove P. acuta to retain attributes for hypoxic tolerance when transferred between habitats. Specifically, we show that mangrove P. acuta coral colonies can survive frequent low O2 exposure (<1.77mg O2 L-1), enabling greater average oxyregulation capacity (Tpos) with increased respiration – while activating non-hypoxia-inducible factor target pathways as an alternative means of anaerobic respiration – compared to populations native to the reef flat. Remarkably, fragments transplanted from the mangrove lagoon to the reef flat exert their maximum regulation capacity (Pcmax) at a lower pO2 level than all other treatments – facilitating their survival during periods of prolonged low-O2 availability. This study highlights that coral populations from extreme ecosystems not only have a greater capacity for oxyregulation, but further, that corals adapted to low O2 environments can retain these traits when moved out of their native system for at least a 1-year period. 

---------------------------------------------------------------------------------------

**Description of the data and file structure** 
This raw data and code has been collected and used in a recent study analysing oxyregulation capacity and hypoxic thresholds for the key reef-building coral species Pocillopora acuta reciprocally transplanted for 1-year period between mangrove lagoons and a reef-flat on the Great Barrier Reef (Dilernia et al. in review). Raw data includes files used to model coral hypoxia response curves (HRCs), as well as P:R Incubations to calculate P:R ratios, and environmental O2 Logger data. 
The raw .csv files used to run the below code, containing data for the *p*O2 (ambient levels of O2 (% air saturation) and VO2 (patterns of O2 consumption, i.e., respiration (mg h-1) values for each species and replicate, across multiple experiments (as outlined in the manuscript), have been included. Files have been separated into experiments, e.g., combined .csv files for the fragmentation experiment can be found in File entitled "Experiment 1 - fragmentation effects", etc.

Date of data collection: February 2023

Geographic location of data collection: Woody Island mangrove lagoon and Low Isles reef flat (GBR, Australia; (~16.388° S, 145.566° E)

Information about funding sources that supported the collection of the data: This research is supported by an Australian Government Research Training Program Scholarship (N.J.D.).

**-->** Link to publication that uses the data: **TBC**

Treatment Groups:
M-R = mangrove to reef transplanted colonies
WR = wild mangrove colonies
R-R = reef to reef transplanted colonies
WR = wild reef colonies

Description of the individual data files/folders:

1. "Abiotic Characterisation (O2 Logger)" Folder
     a. "LoggerCode.Rmd" - code used in RStudio to analyse and visualise the environmental O2 logger data collected in the field from the two habitats (mangrove and reef).
     b. "O2mangrove_reef.csv" - .csv file of raw data collected from the environmental O2 loggers deployed at each habitat.
2. "P-R Incubations (Exp. 1)" Folder
     a. "P-R Measurements.xlsx" - spreadsheet containing P:R measurements taken during incubations, normalisation, and calculation of Net photosynthesis (PN) and respiration (R) rates, determined by calculated changes in O2 during dark and light incubations, and gross photosynthesis (PG) was determined by the addition of PN and R.
3. "Hypoxia Response Curves (HRCs) (Exp. 2)" Folder
     a. This folder includes individual .csv files of raw pO2 and VO2 data from HRCs for each treatment group and replicate, named as "treatment_groupRepX".csv.
     b. "Michaelis-Menten_Modelling.Rmd" - code used in RStudio to model the HRCs with the 2-parameter Michaelis-Menten function.     

Abbreviations:
pO2 - ambient levels of O2 measured (% air sat).
VO2 - standardised rate of O2 consumption over time (mg O2 hr-1).
mg O2 hr-1 or mg O2 L-1 - milligrams of oxygen measured per hour (for VO2) or per litre.
"% air sat" - percentage air saturation of O2 measured.
NB: missing values (empty cells/"NA") in excel spreadsheets: any missing values (i.e., empty cells/NA) in spreadsheets were removed during statistical analyses, i.e., using NA clean up in RStudio.

Code/Software
All statistical analyses were carried out in RStudio version 4.1.0, Build 421 (R Core Team 2021), with base packages: knitr v. 1.33 (Xie 2014, 2015, 2021), rmarkdown v. 2.20 (Xie et al. 2018, 2020; Allaire et al. 2023), and tidyverse v. 2.0.0 (Wickham et al. 2019). Additional modelling, analysis, and plotting packages include: “drc” v. 3.0.1 (Ritz et al. 2015), “ggplot2” (Wickham 2016), “rstatix” version 0.7.2 (Kassambara 2023b), “dplyr” (Wickham et al. 2023).
