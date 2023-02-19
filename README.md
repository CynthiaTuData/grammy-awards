# Grammys' Diversity, 1990-2023
A project analyzing the Grammys' racial diversity

*Read the story here: [The Grammy Awards’ Diversity Problem, in Numbers](https://xinyitu.github.io/grammys/)*
## Goal
The Grammys have been criticized for exlucing artists of color for a long time. With this project, I hope to examine the award's racial inclusivity with data. 

## Data Collection
- Past Grammys nominations were scraped from [Grammy Awards Archive](https://totalmusicawards.com/grammy-awards-winners-archive/). You can check out notebook `grammy-step1-scraping.ipynb` for how the scraping was done.
- The website did not update results for the 2023 Grammys at the time when I started this project. I complied a list of nominations and results from [the Grammys' official site](https://www.grammy.com/news/2023-grammy-nominations-complete-winners-nominees-list). See `2023-grammy.csv`.
## Methodlogy & Analysis
#### Timeframe
This project analyzed Grammys nomination from 1990 to 2023.

#### Award categories
I initially wanted to analyze the "Big Four" Grammys categories, which are Album, Song, Record of the year and Best New Artist.
However, "Song of the Year" is awarded to the songwriter, not the artist/performer. Since my project mostly deals with representation on stage, this categories is omitted for analysis.

#### Artist ethnicity data
Race is a social construct, and its classification changes overtime and in different cultural settings. For this project, I used [ethniccelebs.com](https://ethnicelebs.com/) as the primary source to identify nominees' ethnicity background. For artists whose data is missing on this site, I looked at interviews and media reports of the artist's ethnicity background (self-identified).
- Classification of ethnicity are defined as "white" and "underrepresented" (UR). 
- Artists who are Black/African American, Asian and Pacific Islander, Hispanic/Latino, indigenous descent, and mixed-race are classified as "UR".
- For music groups and bands, race of each member in the group was evaluated. If a member of a group/band is from underrepresented racial group, the nominee is identified as "UR".
- For nomination that features artists who were classified as "UR", the nomination is marked as "UR" and "shared award."

Reference used to develop this methodology: [Inclusion in the Recording Studio?](https://assets.uscannenberg.org/docs/aii-inclusion-recording-studio-20200117.pdf), a study done by the Inclusion Initiative at University of Southern California.

#### Calculating "chance of winning"
Besides the overall racial makeup of nominees and winners, I also looked at the chance of winning by each eacial group as a metric to evaluate whether Recording Academy favors white over non-white musicians. 
Example:

`white nominee chance of winning` = `# of white winners`/`# of total white nominations (winners+nominees)`

For more about the analysis process, check out `grammy-step2-analysis.ipynb`.
## Findings
*Learn more about the findings here: [The Grammy Awards’ Diversity Problem, in Numbers](https://xinyitu.github.io/grammys/)*
![Screen Shot 2023-02-19 at 5 39 04 PM](https://user-images.githubusercontent.com/116761432/219979510-63f89e96-0feb-493d-a2ec-f6b5beeb76fe.png)

- Over the 34 award seasons analyzed, more white artists were nominated than non-white artists.
- More non-white nominees were nominated in recent years

Percentage of non-white nominees across 3 categories over the years
![Screen Shot 2023-02-19 at 5 37 56 PM](https://user-images.githubusercontent.com/116761432/219979463-8ba0b4d8-b81e-4443-ad50-10ef3c10f754.png)

- White nominees stand a higher chance of winning across all three categories analyzed:

![Screen Shot 2023-02-19 at 5 27 56 PM](https://user-images.githubusercontent.com/116761432/219978934-d327af0c-ba11-40a9-a6e4-e6fad131a492.png)


## Challenges and possible improvement
- Data only includes nominations in the past 34 award seasons.
- Data only includes nominations in 3 general categories.
- Subjective bias might have affected the classficiation of white and UR groups. Example:  Artists with European heritage (e.g. Albanian), Hispanic artists, etc.
- Chance of winning and possible biaes did not go through statistical testing.
## Contact
I can be reached at xt2274@columbia.edu or on Twitter @CynthiaTu2. My inbox is open for any comments, suggestions, angry email telling me what I did wrong in this project... 
