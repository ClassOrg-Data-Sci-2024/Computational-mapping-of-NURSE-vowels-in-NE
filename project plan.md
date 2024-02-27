# Sociophonetic study of NURSE vowels in Nigerian English

**Summary**

Studies of NURSE vowel variation across several English varieties in monolingual or bilingual contexts show merging (as a centralized vowel) or maintaining a three-way contrast realized as **[ɪ]**, **[ɛ]**, and **[ʌ]**, with the varied presence of rhotacization. These realizations are influenced by social (e.g. gender, age) and linguistic factors (e.g. speech style). However, very little is known about NURSE vowel variation in New Englishes like Nigerian English (NE), which exists in a rich multilingual context with regional varieties differentiated by speaker L1. This study in a multilingual context may extend the three-way ([ɪ], [ɛ], [ʌ]) or binary (+rhotics, -rhotics) contrast in NURSE vowels and further broaden the explanation of NURSE vowel realization.  

**Data** [ICE-Nigeria]( http://ice-corpora.net/ice/index.html)

International Corpus of English (ICE) Nigeria (ICE-Nig) corpus comprises 609,581 spoken words and 400,796 written words. The corpus hosts text files and speeches for different conversations, including news broadcasts, classroom conversations, non-broadcast shows, interviews, phone calls, conversations, and demonstrations. The website has a metadata Excel file that describes the background information (age, gender, ethnicity, profession, type of speech style) of the participants. 
The sound files will be downloaded (particularly) for participants whose metadata information is complete. After downloading the sound files and the text files for each of the sound files, I will check the text files to clean up the repetition of ‘Transcription 1, Transcription 2…’ that encode participants’ turns because Web MAUS forced aligner does not prefer repetition of (same) text that has no sound representation. After that, I will listen to the sound files to remove clips with a noisy background (in case there are). 
I hope to sample 20 sound files and 150,000+ data points that capture different productions of NURSE vowels. The data points will be elicited through the Fast Track module.


**Method**

Unlike previous studies on NURSE vowels that explored midpoints for NURSE vowel analysis, this study will provide insight into the computational mapping of NURSE vowel analysis that accounts for vowel trajectory during NURSE vowel production. The computation maps vowel production at every 2 milliseconds to capture 5 formant prediction with lowest analysis frequency of 4700Hz and highest analysis frequency of 7550Hz. The raw files will be analyzed using Mixed effects regression that requires **tidyverse**, **lme4** and **PhonR**. 
