

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
Following the forced-aligned segmentation, I have annotated six audio files. These files are **broadcast news** (10) and **broadcast talk** (6). Though I initially planned to annotate three different speech styles, audio annotations took longer than anticipated [read more](https://github.com/ClassOrg-Data-Sci-2024/Sociophonetic-study-of-NURSE-vowels-in-NE/blob/main/Method.md). Second, the forced-aligned segmentation required manual adjustment as the algorithm does not perfectly segment NURSE phonemes in Nigerian English. The manual adjustment was time-consuming, though faster than manual annotation. For now, I would restrict the annotation to broadcast news and talks. If time permits, I will continue annotating other files. Otherwise, I would analyze the annotated files. This serves as a starting point for future studies. Also, I will restrict the inquiry of social variables to broadcast talks because the broadcast news does not have representativeness of different ethnicities, genders, and ages, which are the primary cues for socio-variables. Meanwhile, broadcast talks have these features. In the future, I will carefully annotate audio files with social variables that interest me.

In general, three `csv` files are ready for analysis
1. `nurse_aggregated.csv`
2. `nurse_seg_info`
3. `nurse_vowel.csv`

Each of the files will be used for different levels of analyses.

The overall findings reveal variations in the NURSE vowel of NE, which is significantly different from how other varieties of English (British and American) produce the phenomenon. Also, each variant has a predicted and winning formant for the explanation of phonetic representations of NURSE vowels in NE [realizations](https://github.com/ClassOrg-Data-Sci-2024/Sociophonetic-study-of-NURSE-vowels-in-NE/tree/main/file_images).