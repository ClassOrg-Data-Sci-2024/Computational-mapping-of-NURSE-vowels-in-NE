

# Sociophonetic study of NURSE vowels in Nigerian English

**Oluwasegun Amoniyan**

University of Pittsburgh

Data Science Research for Linguists (LING 2020) Spring 2024



# Motivation for the study

The term `NURSE vowel` means vowels that are produced in similarity or variation to the mid-central vowel (e.g., `[ɜ]` as `[nɜs]` or `[nas]`). The existing literature contains information about NURSE vowel production, particularly in the inner circle of English (Englishes spoken in United States of America, Australia, Canada, United Kingdom). However, their findings often overgeneralize other Englishes (Englishes spoken as second/third language, e.g., Nigeria, Ghana, India, Bangladesh, Tanzania - outer circle of English) without providing any evidence. This study will investigate the phenomenon (NURSE vowel production) in the outer circle of English and provide a balanced description of the variation that characterizes the NURSE vowel production.

## Introduction

NURSE vowels have received scholarly attention in different *varieties* (especially in the inner circle) of English (e.g., *American English*, *British English*, *New Zealand English*). Their results were similar. First, the findings revealed the production of NURSE vowel as centralized vowel or maintaining a four-way contrast realized as [ɜ], [ɪ], [ɛ], and [ʌ] with varied level and presence of rhotics. These variant vowel realizations are influenced by social (e.g., _gender_, _age_), linguistic factors (e.g., _speech style_, _communtiy of practice_) and geographical locations of the speakers (e.g., _urban_ vs _rural_) (Li et. al., 2021; Maclagan et. al., 2017; Mayr, 2010; Mesthrie & Chevalier, 2014; Watson & Clark, 2013). These factors have continued to contribute to the variation in the production of NURSE vowels in Englishes. However, the variant forms of the production were discussed as categorical or gradient `r-less`. In this study, I seek to contribute to the understanding of NURSE vowel variation in sociolinguistics, especially regarding language variation and change in New Englishes.

## Research gap

However, very little is known about NURSE vowel variation in New Englishes like Nigerian English (NE), which exists in a rich multilingual context with regional varieties (i.e., Hausa, Igbo, Yoruba) and over 250 ethnic groups. This study bridges the  gap in the knowledge of NURSE vowel production in Englishes (between inner and outer circle of English). 

- What are NURSE vowel production in NE?
- What possible factors determine variation in NURSE vowel production in NE?
- To what extent do phonetic features describe vowel identity of NURSE vowels?

## Research Hypothesis

The production of NURSE vowels in Nigerian English may vary across **linguistic** (vowel production and phonological context), **ethnicity&languages** (Hausa, Igbo, and Yoruba), and **sociolinguistic** (age, gender, profession) factors. This hypothesis explains the effect of multilingual and diverse sociocultural spaces on NURSE vowel production in Nigerian English. Specifically:

-	NURSE vowel may have variant production in NE

-	Phonological context may affect NURSE vowel production in NE

-	Nigeria has over 200 ethnic groups and three major (Hausa, Igbo, and Yoruba); I hypothesize that ethnicity may determine NURSE vowel production in NE

-	Socio-linguistic factors may determine how NURSE vowels are produced in NE
These factors may contribute to the variation in the production of NURSE vowels than in monolingual speech context.

# Methodology and Data

## Data [ICE-Nigeria]( http://ice-corpora.net/ice/index.html)

International Corpus of English (ICE) Nigeria (ICE-Nig) corpus comprises 609,581 spoken words and 400,796 written words. The corpus hosts `text files` and `audio files` for different discourse, including `broadcast news`, `broadcat talks`, `classroom conversations`, `non-broadcast` shows, `interviews`, `phone calls`, `conversations`, and `demonstrations` (Wunder et al., 2010). The website has a metadata Excel [file](https://sourceforge.net/projects/ice-nigeria/files/) that describes the background (`age`, `gender`, `ethnicity`, `profession`, type of `speech style`) of the participants. Only `broadcast news` and `broadcast talks` were sampled for this study because of the time frame. Specifically, attentions were be paid to different realizations of NURSE vowels across different `profession`, `gender`, `age`, and `ethnicity` in the sampled files. The sound and text files were downloaded and uploaded to [WebMAUS](https://clarin.phonetik.uni-muenchen.de/BASWebServices/interface/WebMAUSBasic) for forced alignment. The textgrids were manually adjusted before the analysis. A total of 246 tokens was extracted from 16 files.

## Fast Track

Fast Track is an automated formant estimation in vowel analysis. The estimation maps vowel production every 2 milliseconds to capture the most continuous formant realization. In each millisecond that the script captures, it reports 5 formant levels, with the lowest as 4700Hz and the highest as 7550Hz. The estimate generates 20 formant samples and selects a winner after comparison with other possible formant outputs. Unlike previous studies of NURSE vowels that implemented midpoint and three-point vowel measurement, Fast Track captures 20 formant points for each vowel production. This algorithm has better formant representation than midpoint and three-point vowel measurement. 

The step-by-step data transformations prior to the analysis are detailed in (data_organization.md)

# Results and Discussion

In this section, I reported on the NURSE vowel variation by phonetic features, social variable and ethnicity. 

## Analysis of NURSE vowel production (phonetics)

In an attempt to answer RQ1, I accounted for the variant production of NURSE vowel in NE,first with length contrast and second without length contrast to identify frequent phoneme for NURSE vowel in NE because vowel length is not sufficient to distinguish vowel in NE. The results that the production of NURSE vowel varied from [nɜs], [na:s], [nas], [nɔs], [nɔ:s], [nɛs] to [ɪ]with different frequency. The most variant form was [nɜs] as [nas] or [nɛs]. These findings revealed that there is a variation in the  production of NURSE vowel in NE. Second, the findings revealed that the variation was not about categorical and gradient production of rhotics in central-mid-vowel, but the phoneme (central-mid-vowel) was realized differently. Also, overall results showed that the NURSE vowel productions are often produced with shorter duration than the longer ones in NE variety.  

![](https://github.com/ClassOrg-Data-Sci-2024/Sociophonetic-study-of-NURSE-vowels-in-Nigerian-English/blob/main/NURSE_analysis_files/figure-gfm/unnamed-chunk-2-1.png)

**Figure 1**

If we are curious about the NURSE vowel space in NE, the results showed that the NURSE vowels are more frequently produced as front vowels (47.56%) than back (45.93%) and central (6.5%). This distribution implied that NE has a somewhat equal proportion of back and front vowels, with back vowels being less common.

However, duration does not seem to significantly determine the variance in NURSE vowel production in NE. The model, the results show that the realization of NURSE vowel as low back vowel ([ɑ]) was statistically significantly differ in duration from other other NURSE vowels (intercept = 0.13, 95%, t(237) = 12.54, p < .001). Meanwhile, among the other variant for NURSE vowels, there was no significant difference (p>0.05). This might reveal that duration was not reliable to differentiate vowels for NURSE production in NE. Rather, vowel height might help to differentiate NURSE vowel variant.

![](https://github.com/ClassOrg-Data-Sci-2024/Sociophonetic-study-of-NURSE-vowels-in-Nigerian-English/blob/main/NURSE_analysis_files/figure-gfm/unnamed-chunk-5-1.png)

**Figure 2**

Similarly, I fitted the second level with `word` (as level 2) and model did not reveal any significant relationship therefore I dropped it from the model. The residual revealed variation across `word` and `vowel` production as 4ms (for `word`) and 3ms (for `vowel`). It means that duration of NURSE vowel in the variety is more variant across `word` than `NURSE vowel`.

One of the hypotheses in the file [method and hypothesis](https://github.com/ClassOrg-Data-Sci-2024/Sociophonetic-study-of-NURSE-vowels-in-Nigerian-English/blob/main/method%20and%20hypothesis/research%20hypothesis.md) identified the effect of phonological environment on NURSE vowel production in NE. To attempt this task, we created a column _nurse_determinant_ where we assigned numeric to each level of the _nurse_vowel_space_ for poisson analysis. The column has three levels: NURSE vowels realized as front vowel, back vowel and central vowel. The numeric _front_vowel = 0_; _back_vowel = 1_, _central_vowel = 2_. 

The model revealed that NURSE vowel productions in NE were affected by phonological environment and the intercept returned significant (p<0.05). Similarly, the random effect for _word_ revealed variation in the vowel production with the standard deviation of 0.2752. Furthermore, the fixed effect estimated for the intercept (-0.5792) indicates the log of vowel productions when no word-specific factor was present. These results supported that the production of vowels in Nigerian English is determined by the phonological environment that NE speakers utter, with various words having variable impacts on vowel formation (see Figure 3, below).

![](https://github.com/ClassOrg-Data-Sci-2024/Sociophonetic-study-of-NURSE-vowels-in-Nigerian-English/blob/main/NURSE_analysis_files/figure-gfm/unnamed-chunk-6-1.png)

The model was extended to investigate whether vowel production in Nigerian English is influenced by the specific _word_ and the speaker's _speech style_ (broadcast interview vs broadcast talk). The model added style (id) to identify if the effect of style would contribute to the variance, but the model failed to converge and I dropped it (id) from the model.

Formant description of NURSE vowels in NE

Though duration was not sufficient to describe differences by length

The formant trajectories for the NURSE vowel production revealed 

What are the formant features of NURSE vowels in NE? 
- What are the formant trajectories of NURSE vowels in NE?
- What insight does multiple selection of formants across time reveal?

## NURSE vowel variation (social variables)

## NURSE vowel variation (ethnicity)

# Conclusion

First, the production of NURSE vowel varies in Nigerian English. Unlike previous studies [link](https://www.cambridge.org/core/journals/journal-of-the-international-phonetic-association/article/what-exactly-is-a-front-rounded-vowel-an-acoustic-and-articulatory-investigation-of-the-nurse-vowel-in-south-wales-english/96F7CC3AC905D8F3DED8E011394310A3), [also](https://journals.sagepub.com/doi/full/10.1177/00754242211025586) in `monolingual context` and these studies explain merger/distinction or varied rhotics; this study, therefore, showed that the more linguistic diverse a speech community (e.g., `bilingual`, `multilingual`) is, the more variation in *NURSE vowel* production. Previous studies on NURSE vowels discussed categorical or gradient rhotacization and their participants were speakers of English as L1. The production of NURSE vowel in NE (a multi-lingual speech community) has revealed inherent variation in the production of NURSE vowel. To this effect, 

##Overall history and process of the project



## Data [ICE-Nigeria]( http://ice-corpora.net/ice/index.html)
