
# Analysis of 12 years of anti-VEGF therapy for neovascular age-related macular degeneration (AMD)

### Problem Statement
Can we identify the main causes of poor vision in patients with AMD?

### Background
In the UK, age-related macular degeneration (AMD) continues to be the leading cause of visual impairment certification. Without treatment, AMD causes irreversible vision deterioration, trouble with many elements of everyday life, and loss of independence. A meta-analysis of untreated eyes in clinical trials indicated that almost 50% had a "significant" decline (≥ 15 EDTRS letters) in vision after 12 months, with a comparable proportion categorised as legally blind (≤35 ETDRS letters).

### Goal

Using statistical methods, we wish to identify those covariates that have a strong relationship with the response variable (good/bad vision).

### Methods
The dataset was extracted from: **Fu, Dun Jack; Keane, Pearse (2020). Insights from survival analyses during 12 years of anti-VEGF therapy for neovascular age-related macular degeneration [Dataset]. Dryad. https://doi.org/10.5061/dryad.nvx0k6dqg**

The it contains the recordings of 7802 patients  recorded  at the Moorfields Eye Clinic, London, UK, and has 14 columns (described further down in the Data dictionary). 
We created a  binary response variable following on the definitions of The Second Report of Age-related Macular Degeneration Audit (AMD) of the National Ophthalmology Database Audit report, where defined the proportion of eyes with “good” visual acuity (≥ 70 ETDRS letters) after one year of treatment and the proportion of eyes with “poor” visual acuity change (≥10 ETDRS letter loss) after one year of treatment.
We also note that no correction for outliers and missing values was made.

### Results 
Where we identify as statistically significant covariates: 
 1. va_inj1_group 
 2. ethnicity 
 3. age_group
 4. loaded 
 5. regimen

### Recommendation
Both the initial VA and the ethnicity are factors of a patients can't be addressed, but in order to prevent lowering the VA of the patient: the treatment should aim to start the younger the patient is, the induction phase should be aimed to be completed within 90 days, and the regimen should be Aflibercept only. Lastly, the gender did not play a role in the VA progression, and neither did the Mean injection interval.

### Risks and Assumptions
The results of this study depend greatly on certain assumptions. The response variable does not apply to all cases on the dataset (originally a different type of study), so there is a loss of data. Furthermore, the data is a cohort of patients from the UK, which must be considered when looking at populations from other areas.

### Data Dictionaries

About MEH_AMD_survivaloutcomes_database.csv file:

Column description:

```
anon_id = anonymised patient number
gender = gender of patient (m = male, f = female)
ethnicity = ethnicity (se_asian [South East Asian], Afro Caribbean, Mixed, Unknown/other)
age_group = age at initiation of anti-VEGF therapy (50-59 years, 60-69 years, 70-79 years, 80 years and above)
va_inj1 = visual acuity at baseline (initiation of anti-VEGF therapy) in early treatment diabetic retinopathy study letter score
va_inj1_group =  visual acuity at baseline grouped (<=35, 36-49, 50-69, >=70)
date_inj1 =  anti-VEGF therapy initiated before October 2013 (pre-2013) or after (post-2013) i.e.  before or after the introduction of aflibercept, respectively
mean_inj_interval = mean interval between injections in induction phase in days
loaded = induction phase was appropriately completed within 90 days (loaded) or not (nonleaded)
time = days following initiation of anti-VEGF therapy
injnum = cumulative number of injection at time
injgiven = whether injection was given at appointment time or not (1 = injections given , 0 = injection not given)
va = visual acuity at time point in early treatment diabetic retinopathy study letter score
regimen = anti-VEGF drug given is ranibizumab (Ranabizumab only) or aflibercept (Aflibercept only)
```

Acronym description:

```
AMD = Age-related Macular Degeneration
VEGF = Vascular Endothelial Growth Factor
VA= Visual Acuity
UK= United Kingdom
ETDRS= The Early Treatment Diabetic Retinopathy Study
```