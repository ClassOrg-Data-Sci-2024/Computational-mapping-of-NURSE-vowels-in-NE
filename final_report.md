

# Sociophonetic study of NURSE vowels in Nigerian English

**Oluwasegun Amoniyan**

University of Pittsburgh

Data Science Research for Linguists (LING 2020) Spring 2024

# Motivation for the study

The term "NURSE vowel" refers to vowels that closely resemble or differ from the mid-central vowel. For example, producing [ɜ] as [nɜs] or [nas]. The existing literature provides information on NURSE vowel creation, particularly in the English inner circle (English spoken in the United States of America, Australia, Canada, and the United Kingdom). However, their conclusions often overgeneralize other Englishes (Englishes spoken as a second or third language, such as Nigeria, Ghana, India, Bangladesh, and Tanzania—the outer circle of English) without presenting proof. This research will look at the phenomenon (NURSE vowel production) in the outer circle of English and present a balanced description of the variance that distinguishes NURSE vowel production.

## Introduction

NURSE vowels have attracted academic attention in several *varieties* of English (particularly in the inner circle), such as *American English*, *British English*, and *New Zealand English*. The outcomes were comparable. First, the data demonstrated that the NURSE vowel is produced as a centralized vowel or maintaining a four-way contrast realized as [ɜ], [ɪ], [ɛ], and [ʌ] with various degrees and the presence of rhotics. These variant vowel realizations are influenced by social (e.g., _gender_, _age_), linguistic factors (e.g., _speech style_, _community of practice_), and geographical locations of the speakers (e.g., _urban_ vs. _rural_) (Heselwood, 2009; Li et al., 2021; Maclagan et al., 2017; Mayr, 2010; Meer, 2023; Mesthrie & Chevalier, 2014; Watson & Clark, 2013). These variables have continued to influence the variance in the creation of NURSE vowels in English. However, the various kinds of production were classified as categorical or gradient 'r-less'. In this work, I want to add to our knowledge of NURSE vowel variation in sociolinguistics, particularly language variation and change in New Englishes.


## Research gap

However, little is known about NURSE vowel variation in New Englishes such as Nigerian English (NE), which occurs in a diverse multilingual setting with regional variations (e.g., Hausa, Igbo, Yoruba) and over 250 ethnic groups. This research fills a knowledge gap about NURSE vowel formation in Englishes (between the inner and outer circle of English). 

- How are NURSE vowels produced in NE?
- What variables might influence variance in NURSE vowel production in NE?
- To what extent do phonetic features describe vowel identity of NURSE vowels?


## Research Hypothesis

The production of NURSE vowels in Nigerian English may vary depending on _linguistic_ (vowel production and phonological context), _ethnicity&languages_ (Hausa, Igbo, and Yoruba), and _sociolinguistic_ (age, gender, occupation). This theory explains how multilingual and diverse sociocultural environments influence NURSE vowel formation in Nigerian English. 
Specifically:

- The NURSE vowel may be produced differently in the NE.- Phonological environment may influence NURSE vowel development in NE.

- Nigeria has around 200 ethnic groupings, including three main ones (Hausa, Igbo, and Yoruba). I predict that ethnicity influences NURSE vowel formation in NE.

- Socio-linguistic variables may impact how NURSE vowels are produced in NE.These variables may lead to variations in the production of NURSE vowels compared to monolingual speech contexts.

# Methodology and Data

## Data [ICE-Nigeria]( http://ice-corpora.net/ice/index.html)

The International Corpus of English (ICE) Nigeria corpus has 609,581 spoken words and 400,796 written words. The corpus contains text and audio files for many discourses, such as broadcast news, broadcast lectures, classroom chats, non-broadcast programs, interviews, phone calls, conversations, and protests (Wunder et al., 2010). The website includes a metadata Excel [file](https://sourceforge.net/projects/ice-nigeria/files/) that summarizes the participants' background (age, gender, ethnicity, and speaking style). Due to time constraints, this research only included broadcast news and broadcast speeches. In particular, the sample files were examined for varied realizations of NURSE vowels across diverse professions, genders, ages, and ethnicities. The sound and text files were downloaded and uploaded to [WebMAUS](https://clarin.phonetik.uni-muenchen.de/BASWebServices/interface/WebMAUSBasic) to ensure alignment. The textgrids were manually changed before analysis. We obtained a total of 246 tokens from 16 files.

## Fast Track

Fast Track is an automatic formant estimate tool for vowel analysis. The estimator maps vowel production every 2 milliseconds in order to capture the most consistent formant realization. The script returns 5 formant timepoints and four formant levels (f1 - f4) for each millisecond captured, with the lowest at 4700Hz and the maximum at 7550Hz, respectively. The estimate creates 20 formant samples and picks a winner by comparing it to other formant outputs. Unlike prior studies on NURSE vowels, which used midpoint and three-point vowel measurement, Fast Track measures 20 formant points for each vowel production. This technique provides better formant representation than midpoint and three-point vowel measurements.

The step-by-step data transformations prior to the analysis are detailed in [analysis folder](https://github.com/ClassOrg-Data-Sci-2024/Sociophonetic-study-of-NURSE-vowels-in-Nigerian-English/blob/main/Analysis/data_organization.md)

# Results and Discussion

In this section, I reported on the NURSE vowel variation by phonetic features, social variable and ethnicity. 

## Analysis of NURSE vowel production (phonetics)

To address RQ1, I accounted for the variation in production of the NURSE vowel in NE, first with length contrast and then without length contrast, to find the frequent phoneme for the NURSE vowel in NE, since vowel length is insufficient to differentiate vowels in NE. The findings showed that the production of NURSE vowel ranged from [nɜs], [na:s], [nas], [nɔs], [nɐ:s], [nɛs] to [ɪ] with variable frequency. The most common variant form was [nɜs] as [nas] or [nɛs]. These studies indicated that there is heterogeneity in the realization of the NURSE vowel in the Northeast. Second, the data demonstrated that the variance was not due to the categorical or gradient creation of rhotics in central-mid-vowel but rather to differences in phoneme realization. Overall, the data demonstrated that NURSE vowel sounds are generally shorter in length than the longer ones in the NE type.

![](https://github.com/ClassOrg-Data-Sci-2024/Sociophonetic-study-of-NURSE-vowels-in-Nigerian-English/blob/main/images/unnamed-chunk-2-1.png)

**Figure 1: Production of NURSE vowel in NE**

Examining the NURSE vowel space in NE reveals a higher production rate of front vowels (47.56%) compared to back (45.93%) or middle (6.5%). This distribution suggests that NE had almost identical numbers of back and front vowels, with back vowels being less prevalent.However, length does not appear to be a major factor in the variation in NURSE vowel production in Nigerian English. The model findings suggest that the realization of the NURSE vowel as a low back vowel ([ɑ]) was statistically significantly different in duration than other NURSE vowels (intercept = 0.13, 95%, t(237) = 12.54, p <.001). Meanwhile, there was no significant difference between the other variants for NURSE vowels (p >0.05). This might indicate that duration was not accurate in distinguishing vowels for NURSE production in NE. Rather, vowel height may help distinguish the NURSE vowel variety.

![](https://github.com/ClassOrg-Data-Sci-2024/Sociophonetic-study-of-NURSE-vowels-in-Nigerian-English/blob/main/images/unnamed-chunk-5-1.png)

**Figure 2: Regression analysis of NURSE vowel duration patterns**

Similarly, I fitted the second level with 'word' (as level 2), and the model revealed no meaningful association; therefore, I removed it from the model. The residual indicated variance in _word_ and _vowel_ production of 4 ms (for _word_) and 3 ms (for _vowel_). It signifies that the length of the NURSE vowel in the variation varies more across the _word_ than the NURSE vowel.

One of the hypotheses in the file [method and hypothesis](https://github.com/ClassOrg-Data-Sci-2024/Sociophonetic-study-of-NURSE-vowels-in-Nigerian-English/blob/main/method%20and%20hypothesis/research%20hypothesis.md) highlighted the influence of phonological environment on NURSE vowel production in Nigerian English. To undertake this job, we established a column _nurse_determinant_ and assigned numeric values to each level of the _nurse_vowel_space_ to allow for poisson analysis. The column is divided into three levels: NURSE vowels, which are realized as front, rear, and center vowels. The numbers _front_vowel = 0_, _back_vowel = 1_, and _central_vowel = 2_. 

The model revealed that NURSE vowel productions in NE were impacted by the phonological environment, with a significant intercept (p<0.05). Similarly, the random effect for _word_ showed variance in vowel production with a standard deviation of 0.2752. Furthermore, when no word-specific factor is present, the calculated fixed effect for the intercept (-0.5792) represents the log of vowel productions. These findings confirmed that the creation of vowels in Nigerian English is regulated by the phonological context in which NE speakers speak, with different words having varying effects on vowel formation (see Figure 3 below).

![](https://github.com/ClassOrg-Data-Sci-2024/Sociophonetic-study-of-NURSE-vowels-in-Nigerian-English/blob/main/images/unnamed-chunk-6-1.png)

**Figure 3: NURSE vowel determinant by phonological environment**

The model was expanded to study whether vowel production in Nigerian English is impacted by the particular _word_ and the speaker's _speech style_ (broadcast interview versus broadcast conversation). The model included style (id) to determine if style's influence contributed to the variance, but the model failed to converge, so I removed it.

However, duration alone wasn't enough to show differences in the length of NURSE vowels. The formant trajectories for the five-point measure showed that (1) there was variation in NURSE vowel production in the formant (f1–f4) and (2) each NURSE vowel variant had a formant trajectory that changed over time. The five-point assessment indicated a variation from one time point to another (SD = 0.09), and the variance within each formant level was 0.11 (residual SD = 0.11) (see Figures 4-5).

![](https://github.com/ClassOrg-Data-Sci-2024/Sociophonetic-study-of-NURSE-vowels-in-Nigerian-English/blob/main/images/unnamed-chunk-8-1.png)

**Figure 4: NURSE vowel formant trajectories**

![](https://github.com/ClassOrg-Data-Sci-2024/Sociophonetic-study-of-NURSE-vowels-in-Nigerian-English/blob/main/images/unnamed-chunk-10-1.png)

**Figure 5: NURSE vowel formant by timepoint**

## NURSE vowel variation (social variables)

Gender and age were major predictors of NURSE vowel production. Female speakers have more diversified vowel production than male speakers. Furthermore, the younger speakers used more varied forms than the older speakers. For example, older male speakers generally realized the vowel as [naes], but younger female and male speakers often generated [nɛs]. The results showed that the production of NURSE vowels was different for people of different ages and genders. This suggests that these factors may have an effect on the production of NURSE vowels in NE (Figure 6).


![](https://github.com/ClassOrg-Data-Sci-2024/Sociophonetic-study-of-NURSE-vowels-in-Nigerian-English/blob/main/images/unnamed-chunk-12-1.png)

**Figure 6: NURSE vowel production by social factors**

Younger Nigerian English speakers had shorter durations for NURSE vowels than adults, although there is no significant association (p = 0.97). Gender showed high statistical relevance (p<0.05). The intercept indicated that male speakers take 2 ms longer than female speakers to produce NURSE vowels (Figures 7, 8).

![](https://github.com/ClassOrg-Data-Sci-2024/Sociophonetic-study-of-NURSE-vowels-in-Nigerian-English/blob/main/images/unnamed-chunk-15-1.png)

**Figure 7a: NURSE vowel duration by social factors**

![](https://github.com/ClassOrg-Data-Sci-2024/Sociophonetic-study-of-NURSE-vowels-in-Nigerian-English/blob/main/images/unnamed-chunk-16-1.png)

**Figure 7b: NURSE vowel duration by social factors**

Random effects indicate small variability in duration, since both within-vowel variance (σ^2) and variation between vowels (τ00) are calculated to be 0.00. The intra-class correlation coefficient (ICC) is predicted to be 0.02, indicating that vowel differences account for a little amount of overall duration variation. 


## NURSE vowel variation (ethnicity)

The production of NURSE vowels depended on ethnicity. Each geographical variation of NE appears to have distinct vowel characteristics. Their characteristics promote variation in NURSE vowels.

![](https://github.com/ClassOrg-Data-Sci-2024/Sociophonetic-study-of-NURSE-vowels-in-Nigerian-English/blob/main/images/unnamed-chunk-17-1.png)

**Figure 8: NURSE vowel production by ethnicity**

In terms of duration, regression analysis revealed no association between Igbo English speakers and NURSE vowel production (p > 0.05); however, Hausa and Yoruba English speakers exhibited a statistically significant relationship in length for NURSE vowels. Meanwhile, when I modeled NURSE vowels, the p-values for vowel creation were insignificant (p > 0.05). That is, despite the fact that there is a variance in length by race, vowel duration patterns showed no link.

![](https://github.com/ClassOrg-Data-Sci-2024/Sociophonetic-study-of-NURSE-vowels-in-Nigerian-English/blob/main/images/unnamed-chunk-19-1.png)

**Figure 9: NURSE vowel duration by ethnicity**

# Conclusion

The NURSE vowel variation in NE indicated (1) that the production of NURSE vowels differed in Nigerian English. Phonetic traits, socioeconomic conditions, and ethnicity all had an impact on this variability.This study showed that the more linguistically varied a speech community (e.g., bilingual, multilingual), the greater the diversity in *NURSE vowel* formation, in contrast to earlier research in monolingual contexts (or when English is dominant). Therefore, the results of NURSE vowels in a multilingual setting went beyond categorical or gradient rhotacization. The NURSE vowel production in the Northeast (a multilingual speech group) has demonstrated intrinsic diversity. This broadens our understanding of the NURSE vowel in English for classification and description.

## Overall history and process of the project

Investigating Nigerian English has long piqued my interest, and I was able to locate a corpus that suited my study's aim. Furthermore, they were well organized in terms of audio and text files. I initially downloaded the audio and text files. Second, I submitted the audio and text files to Web MAUS for forced alignment. Because the variant of English (NE) is understudied, the WebMAUS algorithm proved inaccurate. After the alignment, I had to manually align and visually confirm it. Because this study focuses on NURSE vowel variants, the algorithm has difficulty detecting distinct NURSE vowel productions. For example, whenever the algorithm discovers _ir_, _er_, or _ear_, it transcribes it as the canonical NURSE vowel in British and American. I had to correctly code them, as I discovered. This was a significant challenge and a time-consuming procedure. After that, I used Fast Track to extract data from Praat with Dan's assistance. The project's duration was too short; in the future, I will study any algorithm that is better trained with Nigerian English (NE) and extract more data before generalizing my results. 

## References 

Heselwood, B. (2009). Rhoticity without F3: Lowpass filtering, F1-F2 relations and the perception of rhoticity in NORTH-FORCE, START and NURSE words. Leeds working papers in linguistics and phonetics, 14, 49-64. 

Li, Z., Gut, U., & Schützler, O. (2021). nurse Vowels in Scottish Standard English: Still Distinct or Merged? Journal of English Linguistics, 49(3), 305-330.

Maclagan, M., Watson, C. I., Harlow, R., King, J., & Keegan, P. (2017). Investigating the sound change in the New Zealand English nurse vowel/ᴈ. Australian Journal of Linguistics, 37(4), 465-485.

Mayr, R. (2010). What exactly is a front-rounded vowel? An acoustic and articulatory investigation of the NURSE vowel in South Wales English. Journal of the International Phonetic Association, 40(1), 93-112.

Meer, P. (2023). Variation and change in the NURSE vowel in Trinidadian English: An apparent-time analysis of adolescent and adult speakers. Acquisition and Variation in World Englishes: Bridging Paradigms and Rethinking Approaches, 69, 279.

Mesthrie, R., & Chevalier, A. (2014). Sociophonetics and the Indian diaspora: The NURSE vowel and other selected features in South African Indian English. In English in the Indian diaspora (pp. 85-104). John Benjamins.

Watson, K., & Clark, L. (2013). How salient is the nurse~ square merger? 1. English Language & Linguistics, 17(2), 297-323.

Wunder, E. M., Voormann, H., & Gut, U. (2010). The ICE Nigeria corpus project: Creating an open, rich and accurate corpus. icame Journal, 34(1), 78-88.








