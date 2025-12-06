# Counter Trafficking Data Collaborative (CTDC) North American Analysis

# Introduction
I wanted to approach a gravitational, social science based problem for this analysis. My motivation in working with this specific dataset is the goal of identifying critical risk factors in vulnerable populations across North America (Mexico, The United States, and Canada). If contexts in which a certain population experiences increased vulnerability to trafficking are identified, this awareness could inform policy and increase public awareness.  

Working with human trafficking data requires more than technological prowess, but sensitivity to the biases embedded in the data and in the analyst themselves. Before beginning this analysis, I would like to start by discussing how the data is collected and addressing biases before delving into the analysis.

## The Data and Limitations:

The data: [https://www.ctdatacollaborative.org/dataset/global-synthetic-data-and-resources/resource/microdata]
The codebook: [https://www.ctdatacollaborative.org/dataset/global-synthetic-data-and-resources/resource/codebook]
About Page: [https://www.ctdatacollaborative.org/page/global-synthetic-dataset]

This data contains "critical information on the socio-demographic profile of victims, types of exploitation, and the trafficking process, including means of control used". Containing "over 222,000 victims and survivors of trafficking identified across 197 countries and territories from 2002 to 2023". 

Now I will identify biases and justify some analytical decisions made later on. This is not a complete list of the biases inherint in tasks like this, however it is the three that I found to be most domineering in the literature. 

### I. Population Bias: 

Due to the global nature of this dataset, it is important to follow previous literature in the field's understanding of how different cultures view exploitation differently. Because of this, I have restricted my analysis to the countries of North America in order to most closly align the notion of exploitation with my own. However, that does not mean this bias is irradicated, mearly mitigated. 

### II. Behavioral Bias:

This data is self reported, meaning there is an inescapable bias to its presentation. Certain demographics represented may be more or less likely to report their situations. 

### III. Sampling Bias:

This form of bias is identified by the organization themselves. Due to the collection mechanisms of the data, it only becomes available to the CTDC when reported by partnering organizations. Therefore, it is not a population representative sample. This does not negate its imporance.

# Background or Related Work

The two papers I am using to guide my thinking are:

I. Weitzer, R. (2014). New Directions in Research on Human Trafficking. The ANNALS of the American Academy of Political and Social Science, 653(1), 6-24. https://doi.org/10.1177/0002716214521562 (Original work published 2014)

In this paper, Weitzer identifies the flaws in making sweeping claims about human trafficking data across continents and countries. This paper encouraged me to restrict my analysis to North America, while acknowledging that "the data featured in the global victim of trafficking dataset come from the assistance activities of the contributing organizations, including case management services and counter-trafficking hotline logs." This means all victims were either enrolled in assistance services OR able to contact a hot-line. This is a subset of all human trafficking victims. 

II. Reid, J. A. (2012). Exploratory review of route-specific, gendered, and age-graded dynamics of exploitation: Applying life course theory to victimization in sex trafficking in North America. Aggression and Violent Behavior, 17(3), 257–271. https://doi.org/10.1016/j.avb.2012.02.005

This paper looks at three distinct variables in human trafficking across North America: international vs domestic, male vs female, child vs adult. Here Reid finds "route-specific" vulnerabilities. In other words, differences between trafficking patterns in internationally vs domestically trafficked victims across North America. Here, I will extend this analysis to identify if these patterns are consistent across exploitation types in the CTDC data set. 

# Research Question: What features in the CTDC predict exploitation type in North America? 

# Hypothesis: Victim demographics, control methods, and recruiter relationships will differ between sexual and labor exploitation. 

# Methodology:

I will use logistic regression to create 2 distinct models predicting wether or not a given case will be identified as an instance of sexual or labor exploitation. Because these forms of exploitation are not mututally exclusive (meaning one can experience both), these models had to be distinct. Logistic regression is chosen for its interpretation in terms of the log-likelihood of a case being predicted true or false. 

I will identify the features chosen and discuss any that were derived by me. However, to learn more about the other features, please see the Codebook linked earlier where this is addressed in detail. 

Features Chosen:

    ageBroad: 
        general age bands of victims; these are mapped to numerical categories [1-9]; 0 represents unknown data.
    traffickMonths
    meansDebtBondageEarnings
    meansThreats
    meansAbusePsyPhySex
    meansFalsePromises
    meansDrugsAlcohol
    meansDenyBasicNeeds
    meansExcessiveWorkHours
    meansWithholdDocs
        * note: all means of control features are binarized according to codebook guidelines  
    recruiterRelationIntimatePartner
    recruiterRelationFriend
    recruiterRelationFamily
    recruiterRelationOther
        * note: all recruiter relationship features are binarized according to codebook guidelines  
    gender_Trans/Transgender/NonConforming
    gender_Unknown
    gender_Woman
        Gender is one-hot encoded with men as the reference category, so all reported gender coefficients are interpreted relative to men.
    isCitizenOfCountry
        This is a feature I manually created, where for each entry I check if the countryOfExploitation equals the citizienship feature.

# Findings
    Please see process_data.ipynb for data manipulation and cleaning, and then read analysis.ipynb before reading further. 

# Discussion + Implications
    

# Conclusion

