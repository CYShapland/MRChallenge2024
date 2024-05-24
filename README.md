# MRChallenge2024

This Github page provides necessary data for the 2024 Mendelian Randomization (MR) Conference data challenge.

The MR Data Challenge is an opportunity to explore and develop innovative approaches to causal inference using genetic association data taken from non-european ancestry.

At a glance, these data comprise information on major depressive disorder (MDD) and alcohol use disorder (AUD) their association within African (AFR), East Asian (EAS) and Southeast Asian (SAS) population.

Researchers attending the upcoming 2024 Mendelian randomization conference in Bristol from 19th to 21st June are encouraged to make use of all (or any part) of these data to illustrate new methodology and to compare or explain existing methods as part of an oral presentation.  

A special conference session is being planned to showcase all of the analyses attempted. Individuals will be encouraged to share software and code for transparency and reproducible research. A key aim of the session will be to bring together methodologists and statisticians with experts from medicine, epidemiology and biological science, who will help to comment on and debate the results.

Please circulate widely among your research group and peers if planning to attend the conference, and encourage them to take part

 We look forward to seeing you in Bristol in the summer. Further information on the MR conference is available at https://www.mendelianrandomization.org.uk/.

## Description

The `data` folder in `MRChallenge2024` Github page contains three R data frames with AUD as exposure and MDD as outcome:

1. The data frame `AUD_MDD_AFR_TwoSampleMR.RData` contains cleaned summary data for the estimated associations between AUD and MDD from 196 genetic variants in African ancestry.

2. The data frame `AUD_MDD_EAS_TwoSampleMR.RData` contains cleaned summary data for the estimated associations between AUD and MDD from 182 genetic variants in East Asian ancestry.

3. The data frame `AUD_MDD_SAS_TwoSampleMR.RData` contains cleaned summary data for the estimated associations between problematic alcohol use (PAU, a proxy to AUD) and MDD from 160 genetic variants in South Asian ancestry.

## QC and instrument extraction
"TwoSampleMR" R package v0.6.3 was used to clean and format the raw summary data. Unless specified below, default options were implemented. More details and guidance can be found at https://mrcieu.github.io/TwoSampleMR/index.html. 

### Exposure 
It is important to note that only problematic alcohol use (PAU) is available for SAS ancestry summary data. 

### Instruments for exposure
The clumping significant level for index SNPs was set at $5 \times 10^{-5}$ with 10000 clumping kb window and $r^2$ threshold of 0.001. The SNPs in each datasets (above) contains SNPs with p-value of $5 \times 10^{-5}$ for at least one of the ancestries. The Linkage disequilibrium is calculated using 1000 Genomes data. The genetic corordinates is on the human genome reference sequence (build 37).     

### Outcome
The betas within is log odds ratio from a se-weighted meta-analysis for the effect allele and the sample size is the effective sample size for each variant (calculated as 4/(1/Number of case + 1/Number of control)).

### Harmonise
When harmonising exposure and outcome data, option "Try to infer the forward strand alleles using allele frequency information" was used in `harmonise_data` function.

## Citation

For this challenge we used summary data previously published in Meng et al (1) and Zhou et al (2).

1. Meng, X., Navoly, G., Giannakopoulou, O. et al. Multi-ancestry genome-wide association study of major depression aids locus discovery, fine mapping, gene prioritization and causal inference. Nat Genet 56, 222–233 (2024). https://doi.org/10.1038/s41588-023-01596-4

2. Zhou, H., Kember, R.L., Deak, J.D. et al. Multi-ancestry study of the genetics of problematic alcohol use in over 1 million individuals. Nat Med 29, 3184–3192 (2023). https://doi.org/10.1038/s41591-023-02653-5

## Acknowledgements
I would like to thank Dr Hannah Jones and Dr Christina Dardani for sharing their expertise in their field. TwoSampleMR team for their user-friendly package and quick problem solve. 

## License

This project is licensed under GNU GPL v3.
