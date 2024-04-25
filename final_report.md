

# Sociophonetic study of NURSE vowels in Nigerian English

**Oluwasegun Amoniyan**

University of Pittsburgh

Data Science Research for Linguists (LING 2020) Spring 2024

# Motivation for the study

The term "NURSE vowel" refers to vowels that closely resemble or differ from the mid-central vowel. For example, [ɜ] can be produced as [nɜs] or [nas] depending on the speaker's English variety. The existing literature provides information on NURSE vowel production, particularly in the English inner circle (English spoken in the United States of America, Australia, Canada, and the United Kingdom). However, their conclusions often overgeneralize other Englishes (Englishes spoken as a second or third language, such as Nigeria, Ghana, India, Bangladesh, and Tanzania—the outer circle of English) without evidence. This research therefore investigates Nurse vowel production) in the outer circle of English and presents a balanced description of the variance that explains NURSE vowel variation in NE.

## Introduction

NURSE vowels have attracted scholarly investigation in several *varieties* of English (particularly in the inner circle), such as *American English*, *British English*, and *New Zealand English*. The outcomes were comparable. First, the data showed that the NURSE vowel can be made as a centralized vowel or by keeping a four-way contrast that is made up of [ɜ], [ɪ], [ɛ], and [ʌ], with different levels of rhotics. Factors such as social (e.g., _gender_, _age_), linguistic (e.g., _speech style_, _community of practice_), and geographical (e.g., _urban_ vs. _rural_) play a significant role (Heselwood, 2009; Li et al., 2021; Maclagan et al., 2017; Mayr, 2010; Meer, 2023; Mesthrie & Chevalier, 2014; Watson & Clark, 2013). These variables have continued to influence the variation in the production of NURSE vowels in English. Thus, the literature has established that there is variation in NURSE vowels. Moreover, Collins and Mees (1990) confirm that vowel space (e.g., more front, half-close tongue) distinguishes the variation in NURSE vowels, and they also clarify that duration (i.e., extended duration) influences NURSE vowel productions. Similarly, Penhalurick (2008) adds that the duration determines the degree of openness and a lesser degree of lip-rounding (Wells 1982; Walters 1999) in NURSE vowel production. These studies imply that there is a variation in NURSE vowel production, and the variation differs in gender, age, vowel space, duration, and formant production. In all these studies, social, speech style, duration pattern, vowel space, and geographical factors consistently determine NURSE vowel production. Leaning on the existing studies, this study explains NURSE vowel variation in NE, how phonetic features, social variables and geographical locations describe NURSE vowel production and variation in NE.

## Research Hypothesis

The production of NURSE vowels in Nigerian English may vary depending on _linguistic_ (vowel production and phonological context), _ethnicity&languages_ (Hausa, Igbo, and Yoruba), and _sociolinguistic_ (age, gender, occupation). This theory explains how multilingual and diverse sociocultural environments influence NURSE vowel formation in Nigerian English. Specifically:

- The NURSE vowel may be produced differently in NE.

- Phonological environment may influence NURSE vowel production in NE.

- Nigeria has around 200 ethnic groupings, including three main ones (Hausa, Igbo, and Yoruba). In NE, I predict that ethnicity will influence NURSE vowel production.

- As reported in the existing literature, socio-linguistic variables may determine how NURSE vowels are produced in NE.

# Methodology and Data

## Data [ICE-Nigeria]( http://ice-corpora.net/ice/index.html)

The International Corpus of English (ICE) Nigeria corpus has 609,581 spoken words and 400,796 written words. The corpus contains text and audio files for many discourses, such as broadcast news, broadcast lectures, classroom chats, non-broadcast programs, interviews, phone calls, conversations, and protests (Wunder et al., 2010). The website includes a metadata Excel [file](https://sourceforge.net/projects/ice-nigeria/files/) that summarizes the participants' background (age, gender, ethnicity, and speaking style). Due to time constraints, this research only included broadcast news and broadcast speeches. We specifically examined the sample files for varied realizations of NURSE vowels across diverse professions, genders, ages, and ethnicities. The sound and text files were downloaded and uploaded to [WebMAUS](https://clarin.phonetik.uni-muenchen.de/BASWebServices/interface/WebMAUSBasic) to ensure alignment. Before analysis, we manually recoded the phonome in the textgrids. In all, we obtained a total of 246 tokens from 16 files.

### Data procedure

NE is an under-researched variety of English, and this setback affects prior knowledge about the variety's formant description. The forced aligner was not ideal for the variety; as a result, there were many errors in the surface phoneme output. As a result, after the forced alignment, I perceptually listened to the vowel production and coded it. In the main study, another native speaker would verify the coding to ensure inter-rater reliability. As a native speaker of NE, I listened to the forced aligned segmentation, created a fourth tier, and annotated the NURSE vowel as it was produced. In total, there were seven (7) NE vowels produced as NURSE vowels ([ɒ], [æ], [ɑ], [ɔ], [ɛ], [ɜ], [ɪ]). The step-by-step data transformations prior to the analysis are detailed in the [analysis folder](https://github.com/ClassOrg-Data-Sci-2024/Sociophonetic-study-of-NURSE-vowels-in-Nigerian-English/blob/main/Analysis/data_organization.md).
_NOTE_: There were some _NAs_ (missing values) in the data, and they were purposefully retained as _NAs_ because the ICE-Nig participant sheet was not completely filled out. Also, the term _geographical location_ and _ethnicity_ was used interchangeably because in Nigeria, these ethnic groups are by default differ in geographical location

## Fast Track

Fast Track is a tool for automatic formant estimation for vowel analysis. The estimator maps vowel production every 2 milliseconds in order to capture the most consistent formant realization. The script returns five formant timepoints and four formant levels (f1–f4) for each millisecond captured, with the lowest at 4700 Hz and the maximum at 7550 Hz, respectively. The estimate creates 20 formant samples and picks a winner by comparing them to other formant outputs. Unlike prior studies on NURSE vowels, which used midpoint and three-point vowel measurement, Fast Track measures 20 formant points for each vowel production. This technique provides better formant representation than midpoint and three-point vowel measurements.

# Results and Discussion

In this section, I reported on the NURSE vowel variation by phonetic features, social variables, and ethnicity.

## Analysis of NURSE vowel production (phonetics)

The first RQ was interested in NE's NURSE vowel distinction. The results showed different NURSE vowel production in NE. Unlike Li et al. (2021), who discovered a three-way distinction in the Scottish NURSE vowel, the study revealed that there were five (5) NURSE vowel distinctions in NE.

**Figure 1: NURSE vowel distinction in NE **

As Collins & Mees (1990) projected that NURSE vowel production could vary by vowel space. The frequency distribution revealed the open vowel [e.g., a] as the most frequent variant. For example, the distribution in Figure 1 revealed that low-front and back are the most frequent variants of NURSE, followed by mid-back and mid-front. This result could inform us that NE speakers often produced NURSE vowels as low (front/back), mid-back, or mid-front vowels with different frequencies. However, when explaining NURSE vowel production in NE by position (without height), we discovered a preference for front vowels at 48%, back vowels at 46%, and central vowels at 7%.


Similarly, Penhallurick (2008) suggests that duration also plays a role in determining the degree of mouth openness and lip-rounding in NURSE vowel production. The findings showed that the production of NURSE vowel ranged from [nɒs], [næs], [nɑs], [nɔs], [nɛs], [nɜs] to [nɪs] with differences in duration ([ɑ] -lax, [æ] - tense). The most common variant form was [nɜs] (in British/American English) as [nas] or [nɛs]. These studies indicated that the variety's production of the NURSE vowel is heterogeneous.


**Figure 1: Duration patterns in NE NURSE vowel**

In examining the NURSE vowel duration, the mixed effect model revealed that the production of the NURSE vowel as a low back vowel ([ɑ]) was statistically significantly different in duration than other NURSE vowels (intercept = 0.13, 95%, t(237) = 12.54, p <.001). Meanwhile, there was no significant difference among the other variants for NURSE vowels (p > 0.05). This could indicate that duration was not statistically significant in distinguishing vowels for NURSE production in NE (except for NURSE vowel production as a low back vowel). Rather, vowel height may help distinguish the NURSE vowel variety. Length does not appear to be a major factor in the variation in NURSE vowel production in Nigerian English.

![](https://github.com/ClassOrg-Data-Sci-2024/Sociophonetic-study-of-NURSE-vowels-in-Nigerian-English/blob/main/images/unnamed-chunk-5-1.png)

**Figure 2: Regression analysis of NURSE vowel duration patterns**

In the same way, I fitted the second level with _word_ (as a random effect). The model did not show any meaningful correlation, but the residual showed that there was 4 ms of variation of the NURSE vowel by _word_ and 3 ms by _vowel_. It signifies that the duration of the NURSE vowel in the variation varies more across the _word_ than the NURSE _vowel_.


One of the hypotheses in the file [method and hypothesis](https://github.com/ClassOrg-Data-Sci-2024/Sociophonetic-study-of-NURSE-vowels-in-Nigerian-English/blob/main/method%20and%20hypothesis/research%20hypothesis.md) highlighted the influence of the phonological environment on NURSE vowel production in Nigerian English. To undertake this job, we established a column _nurse_determinant_ and assigned numeric values to each level of the _nurse_vowel_space_ to allow for poisson analysis. I further categorized the vowels into three levels by vowel position: front, back, and center vowels, which represent NURSE vowels. The dummy coding was as follows: _front_vowel = 0_, _back_vowel = 1_, and _central_vowel = 2_.

The model revealed that NURSE vowel productions in NE were impacted by the phonological environment, with a significant intercept (p<0.05). Similarly, the random effect for _word_ showed variance in vowel production with a standard deviation of 0.2752. Furthermore, when no word-specific factor is present, the calculated fixed effect for the intercept (-0.5792) represents the NURSE vowel prediction. These findings confirmed that the phonological context in which NE speakers articulate influences the production of vowels in Nigerian English, with different words having varying effects on vowel production (see Figure 3 below).

![](https://github.com/ClassOrg-Data-Sci-2024/Sociophonetic-study-of-NURSE-vowels-in-Nigerian-English/blob/main/images/unnamed-chunk-6-1.png)

**Figure 3: NURSE vowel determinant by phonological environment**

In the poisson model, phonological effects on the NURSE vowel were investigated. An intercept of 0.60 showed that the baseline phonological prediction for the NURSE vowel was much lower than the reference category. The phonological environment, particularly when the vowel did not follow a consonant, has an incidence rate ratio (IRR) of 0.85, showing a slightly decreased probability of occurrence, though statistically insignificant (p = 0.395). The random effects study shows that the determinant is very different between words, with an intra-class correlation coefficient (ICC) of 0.05. This implies that variations among words account for a portion of the variations in the frequency of production of the NURSE vowel. The model's outcome explained only a small amount of the determinant's variance, with a marginal R-squared value of 0.006 and a conditional R-squared value of 0.059. The model was expanded to examine whether vowel production in Nigerian English is impacted by the particular _word_ and _speech style_ (broadcast interview versus broadcast conversation). The random effects for _word_ and _speech style_ were SD = 22 and SD = 16, respectively. The variation in NURSE vowel production by phonological environment is relatively bigger for _word_ than _speech style_.

Recent studies (Sim et al., 2021; Williams et al., 2015) have emphasized the effect of formant trajectories on vowel identity and behavior. These studies explain the variability between the vowel onset and offset for f1 and f2. The trajectories help to identify whether the NURSE vowels are dynamic or static. It further explains the direction of dynamic vowels.

The mixed effect on formant trajectories revealed a positive and statistically significant relationship, indicating that as time points increase, so does formant. The formant trajectories for the five-point measurement showed that (1) there was variation in NURSE vowel production in the formant (levels of f1–f4) and (2) each NURSE vowel formant had a formant trajectory that changed over time, and these changes varied by formant levels and formant trajectories (see Figure 4). These findings were in accordance with previous studies showing that vowel spectral slice changes over time and helps us know about vowel behavior (Bekker, 2013; Nearey, 2012; Sim et al., 2021; William et al., 2015).

**Figure 5: NURSE vowel formant by timepoint**


## NURSE vowel variation (social variables)

Gender and age were major predictors of NURSE vowel production. Female speakers have more diversified vowel production than male speakers. Furthermore, the younger speakers used more varied forms than the older speakers. For example, older male speakers generally realized the vowel as [næs], but younger female and male speakers often generated [nɛs]. The results showed that the production of NURSE vowels was different for speakers of different ages and genders produced NURSE vowels differently (Figure 6).


![](https://github.com/ClassOrg-Data-Sci-2024/Sociophonetic-study-of-NURSE-vowels-in-Nigerian-English/blob/main/images/unnamed-chunk-12-1.png)

**Figure 6: NURSE vowel production by social factors**

## Phonological effect of NURSE vowels by social variables

In terms of social variables, I hypothesized that the phonological environment, gender, and age category would determine NURSE vowel production. The intercept, 0.61, represents the determinant's baseline occurrence rate. The phonological context, particularly when not coming after a consonant, has a coefficient of 0.28, indicating a minor increase in occurrence rate, albeit statistically insignificant (p = 0.254). Gender and age category (younger) have correlations of -0.08 and 0.14, showing no significant effect on the prediction (p > 0.05). The interaction factors between phonological environment and gender, as well as phonological environment and age category, are statistically insignificant (p > 0.05). The random effects study showed a moderate level of variability in the determinant between terms, with an intraclass correlation value (ICC) of 0.31. Overall, the model explained a small amount of the determinant's variation, with a marginal R-squared value of 0.027 and a conditional R-squared value of 0.324.

**Figure : Effect of phonological environment on NURSE vowels**

## Duration effect of NURSE vowels in NE

The next mixed model examined duration as a factor. When every other factor is zero, the intercept of 0.02 represents the baseline duration for the NURSE vowel. Age group (younger) and gender (male) have negative correlations of -0.02, indicating shorter duration for younger speakers and male speakers compared to their counterparts. The interaction factors for duration and age group, as well as duration and gender, had coefficients of 0.56 and 0.93, respectively. This shows that duration has different effects on different age groups and genders, with younger speakers and male speakers experiencing bigger changes in NURSE vowel duration.

![](https://github.com/ClassOrg-Data-Sci-2024/Sociophonetic-study-of-NURSE-vowels-in-Nigerian-English/blob/main/images/unnamed-chunk-15-1.png)

**Figure 7a: NURSE vowel duration by social factors**

However, the random effects for _word_ show a minimal level of variation in duration between occurrences, with an intra-class correlation coefficient (ICC) of 0.04. This model also reveals the percentage of the variance in duration, with a marginal R-squared value of 0.905 and a conditional R-squared value of 0.909.

## NURSE vowel distinction by ethnicity

The production of NURSE vowels depended on ethnicity. Each geographical variation of NE appears to have distinct vowel characteristics. Their characteristics explained the variation in NURSE vowels.

![](https://github.com/ClassOrg-Data-Sci-2024/Sociophonetic-study-of-NURSE-vowels-in-Nigerian-English/blob/main/images/unnamed-chunk-17-1.png)

**Figure 8: NURSE vowel production by ethnicity**

In terms of duration across geographical location/ethnicity, the linear mixed model investigated how ethnicity influenced the NURSE vowel duration. The intercept for baseline (that is, Hausa) duration was estimated at 0.054, with a standard error of 0.0077 and a highly significant t-value of 6.981 (p < 0.001). Igbo and Yoruba had estimates of -0.003762 and -0.029069, respectively. Yoruba ethnicity's negative coefficient (-0.029069) indicated a shorter duration than the Hausa (reference group), with a significant t-value of -3.629 (p < 0.001). However, the -0.003762 coefficient for Igbo ethnicity is not statistically significant (p = 0.736). The random effects study finds that duration varies across the ethnicity (SD = 0.03) and the word as a standard deviation of 0.04.

![](https://github.com/ClassOrg-Data-Sci-2024/Sociophonetic-study-of-NURSE-vowels-in-Nigerian-English/blob/main/images/unnamed-chunk-19-1.png)

**Figure 9: NURSE vowel duration by ethnicity**

The formant trajectories across the ethnicities were checked, and the models returned did not reveal any statistically significant relationships; however, the estimate values revealed some differences across the ethnicities (see Figure).


# Conclusion

The NURSE vowel variation in NE indicated (1) that the production of NURSE vowels varied in Nigerian English. Phonetic features, sociolinguistic factors, and ethnicity/geographical location all had an impact on this variability. This study showed that the more linguistically varied a speech community (e.g., bilingual, multilingual), the greater the variation in *NURSE vowel* production, in contrast to earlier research in monolingual contexts (or when English is dominant). In the NE (a multilingual speech group), the NURSE vowel production has demonstrated intrinsic diversity. This broadens our understanding of the NURSE vowel in English for classification and description.


## Overall history and process of the project

Investigating Nigerian English has long piqued my interest, and I was able to locate a corpus that suited my study's aim. Furthermore, they were well organized in terms of audio and text files. I initially downloaded the audio and text files. Second, I submitted the audio and text files to Web MAUS for forced alignment. Because the variant of English (NE) is understudied, the WebMAUS algorithm proved inaccurate. After the alignment, I had to manually align and visually confirm it. Because this study focuses on NURSE vowel variants, the algorithm has difficulty detecting distinct NURSE vowel productions. For example, whenever the algorithm discovers _ir_, _er_, or _ear_, it transcribes it as the canonical NURSE vowel in British and American. I had to correctly code them, as I discovered. This was a significant challenge and a time-consuming procedure. After that, I used Fast Track to extract data from Praat with Dan's assistance. The project's duration was insufficient to fully explore an under-researched variety of English (NE) before commencing the project; in the future, I plan to study an algorithm better trained with Nigerian English (NE) and gather more data before generalizing my findings. Also, rather than impressionistic coding without interrater reliability, I will either get a native English speaker for interrater reliability of the NURSE vowel coding or use a k-clustering machine learning algorithm for supervised classification of the NURSE vowel in NE. That said, this research has provided some insight into the NE variety.

## References 

Bekker, I. (2013). Nursing the cure: a phonetic analysis of/ʊə/in South African English. Stellenbosch Papers in Linguistics Plus, 42.

Heselwood, B. (2009). Rhoticity without F3: Lowpass filtering, F1-F2 relations and the perception of rhoticity in NORTH-FORCE, START and NURSE words. Leeds working papers in linguistics and phonetics, 14, 49-64. 

Li, Z., Gut, U., & Schützler, O. (2021). nurse Vowels in Scottish Standard English: Still Distinct or Merged? Journal of English Linguistics, 49(3), 305-330.

Maclagan, M., Watson, C. I., Harlow, R., King, J., & Keegan, P. (2017). Investigating the sound change in the New Zealand English nurse vowel/ᴈ. Australian Journal of Linguistics, 37(4), 465-485.

Mayr, R. (2010). What exactly is a front-rounded vowel? An acoustic and articulatory investigation of the NURSE vowel in South Wales English. Journal of the International Phonetic Association, 40(1), 93-112.

Meer, P. (2023). Variation and change in the NURSE vowel in Trinidadian English: An apparent-time analysis of adolescent and adult speakers. Acquisition and Variation in World Englishes: Bridging Paradigms and Rethinking Approaches, 69, 279.

Mesthrie, R., & Chevalier, A. (2014). Sociophonetics and the Indian diaspora: The NURSE vowel and other selected features in South African Indian English. In English in the Indian diaspora (pp. 85-104). John Benjamins.

Nearey, T. M. (2012). Vowel inherent spectral change in the vowels of North American English. Vowel inherent spectral change, 49-85.

Watson, K., & Clark, L. (2013). How salient is the nurse~ square merger? 1. English Language & Linguistics, 17(2), 297-323.

Wunder, E. M., Voormann, H., & Gut, U. (2010). The ICE Nigeria corpus project: Creating an open, rich and accurate corpus. icame Journal, 34(1), 78-88.

Sims, M., Tucker, B. V., & Nearey, T. M. (2012). Modelling vowel inherent spectral change in spontaneous speech. Canadian Acoustics, 40(3), 36-37.

Williams, D., van Leussen, J. W., & Escudero, P. (2015, August). Beyond North American English: modelling vowel inherent spectral change in British English and Dutch. In ICPhS.

Mayr R. What exactly is a front rounded vowel? An acoustic and articulatory investigation of the nurse vowel in South Wales English. Journal of the International Phonetic Association. 2010;40(1):93-112. doi:10.1017/S0025100309990272 

Collins, B., & Mees, I. M. (1990). The phonetics of Cardiff English. English in Wales: Diversity, Conflict and Change, Nikolas Coupland (ed.), 87-103.

Penhallurick, R. (2008). Welsh English: Phonology. Kortmann et al.(eds.), 105-121.

Wells, John C. 1982. Accents of English. Cambridge: Cambridge University Press.

Walters, Rod. 1999. A study of the segmental and suprasegmental phonology of Rhondda Valleys English. Ph.D. dissertation, University of Glamorgan. http://resnt1.isd.glam.ac.uk/rhondda_valleys_english/ (9 November 2009)

