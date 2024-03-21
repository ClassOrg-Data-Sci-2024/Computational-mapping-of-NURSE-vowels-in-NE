
# Methodology


## Data [ICE-Nigeria]( http://ice-corpora.net/ice/index.html)

The data for this study were drawn from the International Corpus of English Nigeria (ICE-Nig). The corpus contains 1,010,382 collections, with 609,586 spoken words and 400,796 written words (Wunder et al., 2010).  The sound and text files were downloaded and uploaded to WebMAUS for forced alignment. Meanwhile, before the alignment, text files with repetition of ‘Transcription 1, Transcription 2…’ encode participants’ turns were removed because Web MAUS forced aligner did not prefer repetition of (same) text with no sound representation. I hope to sample 10 sound files and 150,000+ data points that capture different productions of NURSE vowels. The data points will be elicited through the Fast Track module. This pilot study includes samples from scripted speeches (broadcast news). The method of this single speech style will be deployed to the remaining broadcast news files and other speech styles.

  
## Speech Style
 
The selected speech styles are considered formal (Thomas, 2011; Labov, 1966, 1972). This genre is assumed to have a standard form of speaking, presumably suitable for pilot study. Second, studies have revealed broadcasters as a model for standard Nigerian English (Akindele, 2020; Melefa, 2018; Oyebola & Gut, 2020).


## Speakers 

All speakers in this study were NE users, including news reporters and newscasters. It should be noted that although they are considered middle-class and upper-class due to their occupations (Isiaka, 2017), their real social class is largely unknown, as mentioned in the corpus. This has consequences for the generalizability of the data. 
 
The total number of **speakers** by **region** (or ethnicity), **education**, **speech styles** and **NURSE vowel variants**,  will be reported after the data elicitation…
 
We did not include any certain token as a predictor because no substantial study has been conducted on NE that explains NURSE vowels in any context. Studies (Di Paolo, 1988; Faber, 1990) discovered vowels before approximants are more likely to be **diphthongized** or undergo a **merger**. This assumption is more useful for varieties of English that codify exceptional words that undergo merger or **diphthongization** (Ladefoged, 2001; Mielke et al., 2019; Schneider et al., 2004). Meanwhile, Thomas (2011) does not discard the inclusion of vowels in the environment of approximants but rather suggests the need for a conscious effort to measure where the vowel is steady and consistent after or before approximants. So, to find out what words cause merger or diphthongization, the initial hypothesis about the phonology of the English variety needs to be written down. However, the variety that has yet to be studied as much, like Nigerian English, doesn't have information about this warning because there hasn't been a study that carefully documents this phenomenon. Thus, including every (content) word class for this study helps us hypothesize based on lexical choices for subsequent studies. No previous research has looked into or discussed this path in NE vowels in the context of citations, connected speech, or sociolinguistic interviews. If reporting approximant effects in this study is successful, it will add to what is known about how language changes and adapts across monolingual, bilingual, and multilingual English. 


## Extraction of NURSE Vowels
 
ICE Nigeria contains automatic phonemic transcriptions created with WebMAUS (Schiel, 2004). The web service creates phonemic transcriptions via forced alignment of orthographical transcriptions and sound files. The transcription will be manually adjusted for both phoneme transcription and the location of onset and offset boundaries marked in Praat (Boersma & Weenink, 2017). I will create TextGrids based on the automatically generated annotations for NURSE vowels to identify NURSE vowel production specifically. Only content words were annotated in this study. These content words include monosyllabic, disyllabic, and polysyllabic words. 
 

## Fast Track

Fast Track is an automated formant estimation in vowel analysis. The estimation maps vowel production every 2 milliseconds to capture the most continuous formant realization. In each millisecond that the script captures, it reports 5 formant levels, with the lowest as 4700Hz and the highest as 7550Hz. The estimate generates 20 formant samples and selects a winner after comparison with other possible formant outputs. Unlike previous studies of NURSE vowels that implemented midpoint and three-point vowel measurement, Fast Track captures 20 formant points for each vowel production. This algorithm has better formant representation than midpoint and three-point vowel measurement. Check [ongoing report](https://github.com/ClassOrg-Data-Sci-2024/Sociophonetic-study-of-NURSE-vowels-in-NE/blob/main/Ongoing%20word%20report.docx)


## Statistical Analysis

The raw files will be analyzed using Mixed effects regression with **tidyverse** and **lme4** to account for social variables that determine (or may contribute to) variation in Nigerian English NURSE vowels.  


