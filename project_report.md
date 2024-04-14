

# Progress Report 1: 02/20/2024

I created the GitHub repository for my final project on sociophonetic study of NURSEvowels in Nigerian English. Similarly, I created files including `README.md` , `gitignore`, `project_plan`, and `progress_report.md`, `method.md.
README.md includes the project title, my name, and a project summary.
 
 - `.gitignore` includes `.raw`, `Rhistory`, `RData`, `.wav`, `.RDataTmp`, `.ice`

 - `project_plan.md` has been created and contains information on the project's scope, as well as plans     for data manipulation and analysis.
 
  - `progress_report.md` has been created with the information that you are now reading


# Progress Report 2: 3/11/2024

-	I have updated the `method.md` file with the proposed method of data selection, elicitation, and analysis procedure. The document was created after reading a chapter on vowel annotation in the Sociophonetic Student’s Guide [read more](https://www.routledge.com/Sociophonetics-A-Students-Guide/Paolo-Yaeger-Dror/p/book/9780415498791). Since there is insufficient information on vowel boundaries and annotation on NE, the chapter is equipped with rationales for my decision. 


-	I have downloaded the audio and the text files. These files were forced aligned in the Web MAUS [Maus](https://clarin.phonetik.uni-muenchen.de/BASWebServices/interface/WebMAUSBasic) 


-	The first phase of the data elicitation were limited to one speech style (broadcast news), and five     files had been annotated. I restricted the annotation to the news casters and news correspondences, the speeches that the correspondents interviewed during the news collection were not annotated. **Rationale** there are no documentation **meta data** of these categories of people on the ICE-Nig website. It is difficult to say about their ethnic affiliation, levels of education, age and gender which are the focus of the project.   


- It's herculean task to treat **(long)audio files** and track where **NURSE vowels** are produced by multilingual speakers. It's time consuming. Bit by bit progress is better than no progress at all.


-	I am test-running FAST TRACK [read more](https://www.degruyter.com/document/doi/10.1515/lingvan-2020-0051/html) to understand how formants are automatically extracted and calculated. After understanding of the algorithm, I will extract two or three files to present the preliminary results. With these results, I will be aware of the data structure for the next thinking about data wrangling. Thereafter, I will annotate other files for `broadcast news` before adding other speech styles.



# Progress Report 3: 4/2/2024

**Accomplishment and RE-consideration**

Following the forced-aligned segmentation, I have annotated six audio files. These files are **broadcast news** (10) and **broadcast talk** (6) [raw_data](https://github.com/ClassOrg-Data-Sci-2024/Sociophonetic-study-of-NURSE-vowels-in-NE/tree/main/raw_Data). Though I initially planned to annotate three different speech styles, audio annotations took longer than anticipated [read more](https://github.com/ClassOrg-Data-Sci-2024/Sociophonetic-study-of-NURSE-vowels-in-NE/blob/main/Method.md). Second, the forced-aligned segmentation required manual adjustment as the algorithm does not perfectly segment NURSE phonemes in Nigerian English. The manual adjustment was time-consuming, though faster than manual annotation. For now, I would restrict the annotation to broadcast news and talks. If time permits, I will continue annotating other files. Otherwise, I would analyze the annotated files. This serves as a starting point for future studies. Also, I will restrict the inquiry of social variables to broadcast talks because the broadcast news does not have representativeness of different ethnicities, genders, and ages, which are the primary cues for socio-variables. Meanwhile, broadcast talks have these features. In the future, I will carefully annotate audio files with social variables that interest me.

In general, three `csv` files are ready for analysis
1. `nurse_aggregated.csv`[read](https://github.com/ClassOrg-Data-Sci-2024/Sociophonetic-study-of-NURSE-vowels-in-NE/blob/main/nurse_raw_aggregated.csv)
2. `nurse_seg_info`[read](https://github.com/ClassOrg-Data-Sci-2024/Sociophonetic-study-of-NURSE-vowels-in-NE/blob/main/nurse_segment_info.csv)
3. `nurse_vowel.csv`[formant at 2ms for multiple times](https://github.com/ClassOrg-Data-Sci-2024/Sociophonetic-study-of-NURSE-vowels-in-NE/blob/main/nurse_vowel.csv)

Each of the files will be used for different levels of analyses.

The overall findings reveal variations in the NURSE vowel of NE, which is significantly different from how other varieties of English (British and American) produce the phenomenon. Also, each variant has a predicted and winning formant for the explanation of phonetic representations of NURSE vowels in NE [realizations](https://github.com/ClassOrg-Data-Sci-2024/Sociophonetic-study-of-NURSE-vowels-in-NE/tree/main/file_images).


# Proposed analysis

# Specific questions to answer in the analysis(Proposed analysis)

A. **Phonetic features**

1. What are the NURSE vowel production (any variation) in NE? (**which** is the over winner in NE variety?) (This identifies how NURSE vowels in NE differs from other English varieties (such as British or American English?)
- What information does this study reveal on the production of NURSE vowel that differs from the previous studies?

2. What are the formant trajectories of NURSE vowels in NE? (*What* insight does multiple selection of *formants* across time reveal?)
 
3. Aside the *formant* which other acoustic cues explain NURSE peculiarities in NE?
  - duration ~ 1 + vowel (1|word) 

4. Do the cutoff for winning formants vary by vowel, gender, ethnicity, or profession? This may further reveal variables that trigger complex in NE NURSE vowels?

B. **Context**

Does context determine NURSE vowel production in NE?
    I expect to see something interesting. 
    duration ~ 1 + (1+vowel|word) (1|speaker)
    *does* the context(`phonological environment`) determine phoneme production for NURSE vowel in NE?
    f3 ~ 1 + (1+vowel|word) (1|speaker)
    *To what extent* does `f3` describe NURSE vowel production in different phonological contexts? (is rhoticization a cue for NURSE vowel in NE)
    
C. **Soical variable (Mixed Effects)**

model 1 = (duration ~ 1 + Age_category + Gender + Ethnicity + Profession_category) (1|Word) + (1|file_name)
model 2 = (duration ~ 1 + Age_category + Gender + Ethnicity + Profession_category) (1|Word) + (1|file_name)
model 3 = (f0 ~ 1 + Age_category + Gender + Ethnicity + Profession_category) (1|Word) + (1|file_name))
(aggregate)
model 3(formant) = f3 (previous studies show *f3* as a cue for *categorical* or *gradient* rhoticization) What does *f3* reveal in this study?  
 (f3 ~ 1 + Vowels)

