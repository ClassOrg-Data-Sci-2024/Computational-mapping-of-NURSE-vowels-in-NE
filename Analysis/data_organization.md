Data Pipeline
================
Oluwasegun Amoniyan
03/27/2024

- [Data summary](#data-summary)
  - [loading raw files](#loading-raw-files)
  - [rename the first column in `nurse_raw_aggregated`before joining the
    dataframes
    together.](#rename-the-first-column-in-nurse_raw_aggregatedbefore-joining-the-dataframes-together)
    - [Working on `nurse_segment_info`](#working-on-nurse_segment_info)
- [Tidy unstructed_seg_info](#tidy-unstructed_seg_info)
  - [Check different NURSE vowel production by audio
    files](#check-different-nurse-vowel-production-by-audio-files)
    - [remove uninformative columns in
      `nurse_segment_info`.](#remove-uninformative-columns-in-nurse_segment_info)
- [NURSE vowel realizations in NE](#nurse-vowel-realizations-in-ne)
- [Combine files](#combine-files)
- [Social variables](#social-variables)
  - [Step 1](#step-1)
  - [Step 2](#step-2)
  - [Step 3](#step-3)
    - [What are the effects of social variables on NURSE
      vowel?](#what-are-the-effects-of-social-variables-on-nurse-vowel)
- [Specific questions to answer in the analysis(Proposed
  analysis)](#specific-questions-to-answer-in-the-analysisproposed-analysis)
  - [Model comparison](#model-comparison)
- [tidy_csv files for analysis](#tidy_csv-files-for-analysis)
- [Session info](#session-info)

``` r
##Set knitr options (show both code and output, show output w/o leading #)
knitr::opts_chunk$set(echo = TRUE, include = TRUE, comment=NA)

#load tidyverse
library(tidyverse)
```

    ## ── Attaching core tidyverse packages ──────────────────────── tidyverse 2.0.0 ──
    ## ✔ dplyr     1.1.4     ✔ readr     2.1.5
    ## ✔ forcats   1.0.0     ✔ stringr   1.5.1
    ## ✔ ggplot2   3.4.4     ✔ tibble    3.2.1
    ## ✔ lubridate 1.9.3     ✔ tidyr     1.3.1
    ## ✔ purrr     1.0.2     
    ## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
    ## ✖ dplyr::filter() masks stats::filter()
    ## ✖ dplyr::lag()    masks stats::lag()
    ## ℹ Use the conflicted package (<http://conflicted.r-lib.org/>) to force all conflicts to become errors

``` r
#load excel
library(readxl)
```

# Data summary

International Corpus of English (ICE) Nigeria (ICE-Nig) corpus comprises
609,581 spoken words and 400,796 written words. The corpus hosts
`text files` and `audio files` for different discourse, including
`broadcast news`, `broadcat talks`, `classroom conversations`,
`non-broadcast` shows, `interviews`, `phone calls`, `conversations`, and
`demonstrations`. The website has a metadata Excel
[file](https://sourceforge.net/projects/ice-nigeria/files/) that
describes the background (`age`, `gender`, `ethnicity`, `profession`,
type of `speech style`) of the participants. Only `broadcast news` and
`broadcast talks` are sampled for the data wrangling and analysis
because of the time frame. Specifically, attention will be paid to
different realizations for NURSE vowels across different `profession`,
`gender`, `age`, and `ethnicity` in the sampled files.

## loading raw files

The first file (as nurse_vowel) includes **nurse_vowel** that contains
**file_name**, **formant trajectories**, **formant bindwidth**,
**pitch**, **intensity** and **harmonity** The second file (as
nurse_segment_info) includes \*segment information\*\*

The second file estimates the aggregate formant means for the winning
acoustic features in the predictions at every 2ms for 20 times per NURSE
vowel realization.

The third file provide segment info such as `context`,
`segment duration`…

``` r
#load raw file
nurse_vowel <- read_excel("C:/Users/oamon/Oluwasegun DS Project/Sociophonetic-study-of-NURSE-vowels-in-NE/untidy_excel/nurse_vowel.xlsx")

nurse_raw_aggregated <- read_excel("C:/Users/oamon/Oluwasegun DS Project/Sociophonetic-study-of-NURSE-vowels-in-NE/untidy_excel/nurse_raw_aggregated.xlsx")

nurse_segment_info <- read_csv("C:/Users/oamon/Oluwasegun DS Project/Sociophonetic-study-of-NURSE-vowels-in-NE/tidy_csv_files/nurse_segment_info.csv")
```

    Rows: 246 Columns: 14
    ── Column specification ────────────────────────────────────────────────────────
    Delimiter: ","
    chr (6): inputfile, file_name, vowel, word, previous_word, next_word
    dbl (8): ...1, interval, duration, start, end, word_interval, word_start, wo...

    ℹ Use `spec()` to retrieve the full column specification for this data.
    ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

## rename the first column in `nurse_raw_aggregated`before joining the dataframes together.

### Working on `nurse_segment_info`

Data cleaning **remove** uninformative columns including `omit`,
`previous_sound` and `next_sound`

``` r
nurse_raw_aggregated <- 
  nurse_raw_aggregated %>%
 rename(
    file_name = contains("þÿfile"))
head(nurse_raw_aggregated)
```

    # A tibble: 6 × 28
      file_name     f0 duration_ms label group color number cutoff   f11   f21   f31
      <chr>      <dbl>       <dbl> <chr> <dbl> <chr>  <dbl>  <dbl> <dbl> <dbl> <dbl>
    1 bnew_01_0…  192.       0.078 "\u0…    30 Navy       1   6058   514   973  2516
    2 bnew_01_0…  233.       0.098 "\u0…    30 Navy       2   4992   653  1108  2242
    3 bnew_01_0…  295.       0.084 "\u0…    26 Black      3   6484   942  1749  2678
    4 bnew_01_0…  304.       0.078 "\u0…    26 Black      4   5632   670  1523  2671
    5 bnew_01_0…  284.       0.108 "\u0…    25 Mage…      5   4992   851  1421  2424
    6 bnew_01_0…  252.       0.096 "\u0…    26 Black      6   4779   550  1022  2207
    # ℹ 17 more variables: f41 <dbl>, f12 <dbl>, f22 <dbl>, f32 <dbl>, f42 <dbl>,
    #   f13 <dbl>, f23 <dbl>, f33 <dbl>, f43 <dbl>, f14 <dbl>, f24 <dbl>,
    #   f34 <dbl>, f44 <dbl>, f15 <dbl>, f25 <dbl>, f35 <dbl>, f45 <dbl>

``` r
nurse_raw_aggregated <- nurse_raw_aggregated%>%
mutate(files = map_chr(file_name, ~ str_sub(.x, 1, 7)))
head(nurse_raw_aggregated)
```

    # A tibble: 6 × 29
      file_name     f0 duration_ms label group color number cutoff   f11   f21   f31
      <chr>      <dbl>       <dbl> <chr> <dbl> <chr>  <dbl>  <dbl> <dbl> <dbl> <dbl>
    1 bnew_01_0…  192.       0.078 "\u0…    30 Navy       1   6058   514   973  2516
    2 bnew_01_0…  233.       0.098 "\u0…    30 Navy       2   4992   653  1108  2242
    3 bnew_01_0…  295.       0.084 "\u0…    26 Black      3   6484   942  1749  2678
    4 bnew_01_0…  304.       0.078 "\u0…    26 Black      4   5632   670  1523  2671
    5 bnew_01_0…  284.       0.108 "\u0…    25 Mage…      5   4992   851  1421  2424
    6 bnew_01_0…  252.       0.096 "\u0…    26 Black      6   4779   550  1022  2207
    # ℹ 18 more variables: f41 <dbl>, f12 <dbl>, f22 <dbl>, f32 <dbl>, f42 <dbl>,
    #   f13 <dbl>, f23 <dbl>, f33 <dbl>, f43 <dbl>, f14 <dbl>, f24 <dbl>,
    #   f34 <dbl>, f44 <dbl>, f15 <dbl>, f25 <dbl>, f35 <dbl>, f45 <dbl>,
    #   files <chr>

# Tidy unstructed_seg_info

`unstructed_seg_info` has segment features for NURSE vowels.

``` r
#before joining nurse_segment_info with the aggregate by outputfile, there must be a similar name between the two dataframes 
nurse_segment_info <- 
  nurse_segment_info %>%
 rename(
    file_name = contains("outputfile"))
head(nurse_segment_info)
```

    # A tibble: 6 × 14
       ...1 inputfile file_name    vowel interval duration start   end word    
      <dbl> <chr>     <chr>        <chr>    <dbl>    <dbl> <dbl> <dbl> <chr>   
    1     1 bnew_01   bnew_01_0001 ɔ            2   0.0782  37.1  37.2 worse   
    2     2 bnew_01   bnew_01_0002 ɔ            4   0.0994  91.4  91.5 urge    
    3     3 bnew_01   bnew_01_0003 ɒ            6   0.0855 159.  159.  thursday
    4     4 bnew_01   bnew_01_0004 ɒ            8   0.0800 161.  161.  occurred
    5     5 bnew_01   bnew_01_0005 ɑ           10   0.109  183.  183.  swerved 
    6     6 bnew_01   bnew_01_0006 ɒ           12   0.0964 220.  220.  working 
    # ℹ 5 more variables: word_interval <dbl>, word_start <dbl>, word_end <dbl>,
    #   previous_word <chr>, next_word <chr>

## Check different NURSE vowel production by audio files

``` r
nurse_segment_info %>%
  select(inputfile)%>%
  table()
```

    inputfile
    bnew_01 bnew_02 bnew_03 bnew_04 bnew_05 bnew_06 bnew_07 bnew_08 bnew_09 bnew_10 
          9      10       6       8      11      24       9      16      13      19 
    btal_01 btal_04 btal_21 btal_22 btal_33 btal_36 
         16      14      35      22      15      19 

### remove uninformative columns in `nurse_segment_info`.

The following columns(`previous_sound`, `next_sound` and `omit`) are
dropped in the `nurse_segment_info` because they add no value to the
`dataframe`.

``` r
#nurse_segment_info <- nurse_segment_info %>%
 # select(-c("previous_sound", "next_sound", "omit"))
```

**Hurray** `nurse_segment_info` is now tidy

# NURSE vowel realizations in NE

``` r
nurse_segment_info%>%
  select(vowel)%>%
  table()
```

    vowel
     ɑ  ɒ  æ  ɔ  ɛ  ɜ  ɪ 
    32 39 67 42 49 16  1 

# Combine files

combine both files as a single `csv` file before `data analysis`

``` r
#combined_data <- merge(nurse_segment_info, nurse_raw_aggregated, by = "file_name")
#view(combined_data)
```

# Social variables

`Social variable` dataset was extracted from the participants
[ICE-Nigeria](http://ice-corpora.net/ice/index.html) to account for how
social variables (e.g., `age`, `profession`, `gender`)

## Step 1

Read the data

``` r
nurse_social_var <- read_excel("C:/Users/oamon/Oluwasegun DS Project/Sociophonetic-study-of-NURSE-vowels-in-NE/untidy_excel/nurse_social_var.xlsx",
                                     na=c("", "Na", "NA", "N/A", "n/a", "na", "-"))
head(nurse_social_var)
```

    # A tibble: 6 × 5
      files   Gender   Age Ethnicity Profession     
      <chr>   <chr>  <dbl> <chr>     <chr>          
    1 bnew_01 female    23 Igbo      Radio presenter
    2 bnew_02 female    47 Yoruba    Radio presenter
    3 bnew_03 female    NA Yoruba    TV  presenter  
    4 bnew_04 male      NA Yoruba    TV journalist  
    5 bnew_05 male      NA Yoruba    TV  journalist 
    6 bnew_06 female    37 Yoruba    TV journalist  

## Step 2

**Re-categorize** the `profession` column into `broadcaster` and
`politician` rather than the original column that has `Radio presenter`,
`TV presenter`, `TV journalist`, and `Politician`

``` r
nurse_social_var <- nurse_social_var %>%
  filter(Profession %in% c("Radio presenter", "TV presenter", "TV journalist", "Politician"))%>%
  mutate(Profession_category = ifelse(Profession %in% c("Radio presenter", "TV presenter", "TV journalist"), "Broadcaster", "Politician"))
head(nurse_social_var)
```

    # A tibble: 6 × 6
      files   Gender   Age Ethnicity Profession      Profession_category
      <chr>   <chr>  <dbl> <chr>     <chr>           <chr>              
    1 bnew_01 female    23 Igbo      Radio presenter Broadcaster        
    2 bnew_02 female    47 Yoruba    Radio presenter Broadcaster        
    3 bnew_04 male      NA Yoruba    TV journalist   Broadcaster        
    4 bnew_06 female    37 Yoruba    TV journalist   Broadcaster        
    5 bnew_08 male      NA Yoruba    TV journalist   Broadcaster        
    6 bnew_09 male      NA <NA>      TV journalist   Broadcaster        

## Step 3

**Re-categorize** the `age` column into `younger` and `older` rather
than the original column that has `numerical values`. The original
column has between 20 and 75 years. The new category groups ages between
20 and 45 as younger, 46 and above as older

``` r
nurse_social_var <- nurse_social_var %>%
  filter(Age %in% c(23, 47, 37, 76, 54, 53, 42, 46))%>%
  mutate(Age_category = ifelse(Age %in% c(23, 37, 42), "younger", "older"))
head(nurse_social_var)
```

    # A tibble: 6 × 7
      files   Gender   Age Ethnicity Profession     Profession_category Age_category
      <chr>   <chr>  <dbl> <chr>     <chr>          <chr>               <chr>       
    1 bnew_01 female    23 Igbo      Radio present… Broadcaster         younger     
    2 bnew_02 female    47 Yoruba    Radio present… Broadcaster         older       
    3 bnew_06 female    37 Yoruba    TV journalist  Broadcaster         younger     
    4 btal_22 male      76 Hausa     Politician     Politician          older       
    5 btal_21 male      54 Hausa     Politician     Politician          older       
    6 btal_04 male      53 Igbo      Politician     Politician          older       

### What are the effects of social variables on NURSE vowel?

To calculate the effect of social variables on NURSE vowel,
`nurse_social_var` and `nurse_segment_info` data frames are joined by
files.

``` r
#nurse_soc_segment <- merge(nurse_segment_info, nurse_social_var, by = "files")
```

The dataframe **nurse_soc_segment** has segment info such as `vowel`,
`duration_ms`,
start_dur_sec`,`end_dur_sec`,`word`,`word_interval`,`dur_word_start`,`dur_word_end`,`previous_word`,`next_word`,`gender`,`Age_category`,`Profession_category\`.

# Specific questions to answer in the analysis(Proposed analysis)

A. **Phonetic features**

1.  What are the NURSE vowel production (any variation) in NE?
    (**which** form is the most frequent in NE variety?) (This
    identifies how NURSE vowels in NE differs from other English
    varieties (such as British or American English?)

- What information does this study reveal on the production of NURSE
  vowel that differs from the previous studies?

2.  What are the formant trajectories of NURSE vowels in NE? (*What*
    insight does multiple selection of *formants* across time reveal?)

3.  Aside the *formant* which other acoustic cues explain NURSE
    peculiarities in NE?

- duration ~ 1 + vowel (1\|word)
- intensity ~ 1 + vowel (1\|word)

4.  Do the cutoff for winning formants vary by vowel, gender, ethnicity,
    or profession? This may further reveal variables that trigger
    complex in NE NURSE vowels?

B. **Context** Does context determine NURSE vowel production in NE? I
expect to see something interesting. duration ~ 1 + (1+vowel\|word)
(1\|speaker) *does* the context(`phonological environment`) determine
phoneme production for NURSE vowel in NE? f3 ~ 1 + (1+vowel\|word)
(1\|speaker) *To what extent* does `f3` describe NURSE vowel production
in different phonological contexts? (is rhoticization a cue for NURSE
vowel in NE)

C. **Soical variable (Mixed Effects)** model 1 = (duration ~ 1 +
Age_category + Gender + Ethnicity + Profession_category) (1\|Word) +
(1\|vowel) + (1\|file_name) model 2 = (f0 ~ 1 + Age_category + Gender +
Ethnicity + Profession_category) (1\|Word) + (1\|vowel) +
(1\|file_name)) model 3 = (aggregate) model 3(formant) = f3 (previous
studies show *f3* as a cue for *categorical* or *gradient*
rhoticization) What does *f3* reveal in this study?  
(f3 ~ 1 + Vowels)

### Model comparison

# tidy_csv files for analysis

``` r
write_csv(nurse_social_var, "nurse_social_var.csv")
write_csv(nurse_raw_aggregated, "nurse_raw_aggregated.csv")
write_csv(nurse_segment_info, "nurse_segment_info.csv")
write_csv(nurse_vowel, "nurse_vowel.csv")
```

# Session info

``` r
sessionInfo()
```

    R version 4.3.2 (2023-10-31 ucrt)
    Platform: x86_64-w64-mingw32/x64 (64-bit)
    Running under: Windows 11 x64 (build 22631)

    Matrix products: default


    locale:
    [1] LC_COLLATE=English_United States.utf8 
    [2] LC_CTYPE=English_United States.utf8   
    [3] LC_MONETARY=English_United States.utf8
    [4] LC_NUMERIC=C                          
    [5] LC_TIME=English_United States.utf8    

    time zone: America/New_York
    tzcode source: internal

    attached base packages:
    [1] stats     graphics  grDevices utils     datasets  methods   base     

    other attached packages:
     [1] readxl_1.4.3    lubridate_1.9.3 forcats_1.0.0   stringr_1.5.1  
     [5] dplyr_1.1.4     purrr_1.0.2     readr_2.1.5     tidyr_1.3.1    
     [9] tibble_3.2.1    ggplot2_3.4.4   tidyverse_2.0.0

    loaded via a namespace (and not attached):
     [1] bit_4.0.5         gtable_0.3.4      crayon_1.5.2      compiler_4.3.2   
     [5] tidyselect_1.2.0  parallel_4.3.2    scales_1.3.0      yaml_2.3.8       
     [9] fastmap_1.1.1     R6_2.5.1          generics_0.1.3    knitr_1.45       
    [13] munsell_0.5.0     pillar_1.9.0      tzdb_0.4.0        rlang_1.1.3      
    [17] utf8_1.2.4        stringi_1.8.3     xfun_0.41         bit64_4.0.5      
    [21] timechange_0.3.0  cli_3.6.1         withr_3.0.0       magrittr_2.0.3   
    [25] digest_0.6.34     grid_4.3.2        vroom_1.6.5       rstudioapi_0.15.0
    [29] hms_1.1.3         lifecycle_1.0.4   vctrs_0.6.5       evaluate_0.23    
    [33] glue_1.7.0        cellranger_1.1.0  fansi_1.0.6       colorspace_2.1-0 
    [37] rmarkdown_2.25    tools_4.3.2       pkgconfig_2.0.3   htmltools_0.5.7  
