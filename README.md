# MRChallenge2024

This Github page provides necessary data for the 2024 Mendelian Randomization (MR) Conference data challenge.

The MR Data Challenge is an opportunity to explore and develop innovative approaches to causal inference using genetic association data taken from non-european ancestry.

At a glance, these data comprise information on major depressive disorder (MDD) and alcohol use disorder (AUD) their association within African (AFR), East Asian (EAS) and Southeast Asian (SAS) population.

Researchers attending the upcoming 2024 Mendelian randomization conference in Bristol from 19th to 21st June are encouraged to make use of all (or any part) of these data to illustrate new methodology and to compare or explain existing methods as part of an oral presentation.  

A special conference session is being planned to showcase all of the analyses attempted. Individuals will be encouraged to share software and code for transparency and reproducible research. A key aim of the session will be to bring together methodologists and statisticians with experts from medicine, epidemiology and biological science, who will help to comment on and debate the results.

Please circulate widely among your research group and peers if planning to attend the conference, and encourage them to take part

 We look forward to seeing you in Bristol in the summer. Further information on the MR conference is available at https://www.mendelianrandomization.org.uk/.

## Description

The `MRChallenge2024` Github page contains three data frames:

1. The data frame `Challenge_dat` contains summary data for the estimated associations between 118 metabolite risk factors and 150 genetic variants, with metabolite information quantified using nuclear magnetic resonance (NMR) spectroscopy metabolomics. The data also includes information on 7 outcomes; age-related macular degeneration, alzheimers's disease, type 2 diabetes, Ischemic stroke, large artery stroke, cardioembolic stroke, and small vessel stroke.

2. The data frame `NMRA_dat` contains the abbreviation, full name, overall heritability of the trait, and classification of each NMR trait.

3. Running the command `vignette("challenge")` will display a document giving a detailed description of the data and broad aims of the data challenge.


## Citation

For this challenge we used summary data previously published in Meng et al (1) and Zhou et al (2).

1. Meng, X., Navoly, G., Giannakopoulou, O. et al. Multi-ancestry genome-wide association study of major depression aids locus discovery, fine mapping, gene prioritization and causal inference. Nat Genet 56, 222–233 (2024). https://doi.org/10.1038/s41588-023-01596-4

2. Zhou, H., Kember, R.L., Deak, J.D. et al. Multi-ancestry study of the genetics of problematic alcohol use in over 1 million individuals. Nat Med 29, 3184–3192 (2023). https://doi.org/10.1038/s41591-023-02653-5

## License

This project is licensed under GNU GPL v3.
