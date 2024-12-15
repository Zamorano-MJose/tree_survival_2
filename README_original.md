# Dataset for "Tree seedling shade tolerance arises from interactions with microbes and is mediated by functional traits"

***

We conducted a fully factorial blocked-design greenhouse experiment at the Michigan State University Tree Research Center in Lansing, Michigan, USA (42.7 ºN, 84.5 ºW). The experiment consisted of three species, four microbial communities (&lt;20 µm, representing pathogenic microbes; 40-250 µm, representing AMF; combined filtrate (both &lt;20 µm and 40-250 µm); and sterilized combined filtrate) and two light levels (2% and 30% full sun, representing shade and light gap environments). Individual pots were set up on six different benches (three per light level), where all treatment combinations were represented. We planted 80 seedlings per treatment combination for a total of 1,920 seedlings. We monitored seedlings every three days for survival, and randomly selected subsets for trait measurements (percent colonization by arbuscular mycorrhizal fungi, phenolics, lignin, and nonstructural carbohydrates) at three, six, and nine weeks. Data were collected 2016-2017.

## Description of the data and file structure

There are two included files. A .csv file containing data and a .txt file with the survival model.

In the .csv file, we include measured trait, survival, and imputated trait data for the greenhouse experiment. Detailed information about each column follows:

* **No:** Seedling unique ID number
* **Species:** 3 Temperate tree species that co-occur within the same forest, belong to the same genus, but vary in shade tolerance
    * Acsa = *Acer saccharum*
    * Acru = *Acer rubrum*
    * Acne = *Acer negundo*
* **Light:** Light levels were created using shade cloth over greenhouse benches
    * Low = 2% full sunlight
    * High = 30% full sunlight
* **Microbe:** Microbial filtrates were acquired through the wet-sieving method (see manuscript for more details)
    * Control = sterilized Combined filtrate, used only in supplementary analyses
    * None = deionized water + filter paper
    * Small = &lt;20µm filtrate in deionized water + filter paper
    * Large = deionized water + 40-250µm filtrate on filter paper
    * Combined = both &lt;20µm filtrate in deionized water + 40-250µm filtrate on filter paper
* **Adult:** Number of the adult tree used for soil collection; used as a random effect in analyses; up to 4 per species
* **Bench:** Number of the bench each seedling was grown on; used as a random effect in analyses
* **Harvest:** Time (in weeks) that the seedling was harvested (if at all) for trait measurement
    * 3, 6, or 9 weeks
* **Time:** Number of days into the experiment, at which time the seedling either was harvested, died, or the experiment ended
* **Event:** Used for survival analysis to indicate status of each individual seedling at a given time (above)
    * 0 = harvested or experiment ended
    * 1 = dead
* **AMF:** Calculated as AMF Count / AMF Intersections for percent colonization by AMF (see manuscript for detailed methods)
* **Phenolics:** Calculated as nmol Gallic acid equivalents per mg dry extract (see manuscript for detailed methods)
* **NSC:** Calculated as percent dry mass nonstructural carbohydrates (see manuscript for detailed methods)
* **Lignin:** Calculated as percent dry mass lignin (see manuscript for detailed methods)
* **AMF\_Imp:** Percent colonization AMF, imputated from measured data for analyses of trait relationships with survival
* **PHN\_Imp:** Phenolic content, imputated from measured data for analyses of trait relationships with survival
* **NSC\_Imp:** Percent dry mass nonstructural carbohydrates, imputated from measured data for analyses of trait relationships with survival
* **LIG\_Imp:** Percent dry mass lignin, imputated from measured data for analyses of trait relationships with survivalSharing/Access information


Missing data is coded as NA. 

## Sharing/Access Information

There are no licenses or restrictions placed on the data (public domain). All data was collected from this single experiment and is presented in the associated manuscript: Wood KEA, Kobe RK, McCarthy-Neumann S. 2023*.* Tree seedling shade tolerance arises from interactions with microbes and is mediated by functional traits. *Frontiers in Ecology and Evolution.*

For any questions about the manuscript or dataset, including methodology and availability, please contact the corresponding author: Katherine EA Wood, woodkat7@msu.edu. 

## Code/Software

We performed all analyses in R 3.5.1 (R Core Team, 2020). We used the *rjags* package (Plummer, 2019) to fit survival models and to run predicted survival and contrast simulations. We used the built-in “lmer” function to fit linear mixed effects models and tested significance of main effects using the “Anova” function in the *car* package (Fox &amp; Weisberg, 2019). Model selection for linear mixed effects models was determined with the “step” function in the *lmerTest* package (Kuznetsova et al., 2017). Post-hoc Tukey pairwise comparisons of significant main effects were made using the “emmeans” and “joint\_tests” functions in the *multcomp* package (Hothorn et al., 2008; Lenth, 2020).

surv-model.txt includes the survival model to be run through RJags in R. Software and package versions should not matter, since the text file is just the model structure.