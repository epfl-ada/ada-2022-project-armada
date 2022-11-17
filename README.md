# Is the cinema sexist ?

## Abstract :memo:
<!---
A 150 word description of the project idea and goals. What’s the motivation behind your project? What story would you like to tell, and why?)
--->
The CMU Movie Summary Corpus provides a collection of 42,306 movie plot summaries and metadata at both the movie level (including box office revenues, genre and date of release) and character level (including gender and estimated age). 
We aim to assess the evolution over time of the presence of women in the film industry. First, we focus on the proportion of actresses in the casting of a film. Then, we study the impact of women by looking at features of the characters played by these actresses in the most successfull movies using the Stanford CoreNLP-processed summaries. Finally, we look at the evolution over time and offer an historical perpective.

## Research Questions :grey_question:
<!---
A list of research questions you would like to address during the project.
--->
During the project we would like to adress the following questions to try to answer our problematic.

1. What is the ratio of women to men in cinema ?
1. What is the impact of women in cinema?
1. Do these answers change over time ?

<a name="additional-datasets"></a>
## Additional Datasets :fax:
<!---
List the additional dataset(s) you want to use (if any), and some ideas on how you expect to get, manage, process, and enrich it/them.
Show us that you’ve read the docs and some examples, and that you have a clear idea on what to expect. Discuss data size and format if relevant.
It is your responsibility to check that what you propose is feasible.
--->
To deepen the analysis and recover the missing values, we use additionnal datasets from IMDB:

* [Country API](https://restcountries.com/): Lists countries by world region in order to sort each film in the database by region rather than by country. 

* [title.ratings](https://www.imdb.com/interfaces/): provides **IMDB average rating** and **number of votes** for more than a million of movies and series. This additionnal information allows us to quantify the success and the popularity of a movie and then complete the information provided by the box office revenue in the Freebase Movie dataset which contains around 90% of missing values. 

* [title.crew](https://www.imdb.com/interfaces/): provides the **directors and writers names** for more than a million of films and series. This enrich the analysis made on the ratio of women to man and their impact in cinema by regarding not only the actress but also the writers and directors distribution.

* [Stanford CoreNLP-processed summaries](http://www.cs.cmu.edu/~ark/personas/): contains all the processed summaries from the FreeBase movie database. The process consists in extracting for each character the agent and patent verbs and attributes related to him. This structure reveals the actions they take on others, the actions done to them, and the attributes by which they are described. More details are available in [this article](http://www.cs.cmu.edu/~dbamman/pubs/pdf/bamman+oconnor+smith.acl13.pdf).


The link between the **Freebase movie ID** with the **IMDB movie ID** (*tconst*) is made using 3 matching criteria: `Movie Name`, `Movie Release Date` and `Movie Runtime`. This brings us to about 45,000 matches out of 80,000 films in the Freebase database.

## Methods :mag:

After our first analyses of the data, we chose to make some hypothesis for our futur work :
- Knowing that the paper as been published in 2013, we will only consider movies until 2012 and not the few movies that have release dates between 2013 and 2016.
- We will only consider the five principal movie genres, which are : drama, comedy, romance, action and thriller. "Black and white" is listed as a genre in the dataset and is the forth more represented one but we chose not to consider it. Indeed, it does not seem to be a genre that will be meaningful in the analysis about the impact of women in cinema.

> ### What is the ratio of women to men in cinema ?
> 1. To start our investigation, we first explore ratio of women to men in cast overall, then by sorting by region or by gender. 
> 2. Then, we carry out the same analysis using the additionnal crew database from IMDB.  
> 3. Finally, we will try to determine whether there is a correlation between the ratio of women in the film crew and in the film cast.
>
>Although the proportion of women in the industry can give us some good initial indicators as to the film industry's gender gap, it omits an even more important indicator. What is the representation of women in these films? Are they playing strong, impactful characters or are they playing roles dominated by men? 

> ### What is the impact of women in cinema?
> 1. As a first approach, we are interested in the representation of women in popular films, regarding both the box office revenue and number of votes on IMDB (from the additionnal dataset). Considering the IMDB score, the analysis continues by studying this time the representation of women in the well-received films.
> 2. By working with the [Stanford CoreNLP-processed summaries](http://www.cs.cmu.edu/~ark/personas/), we expect to develop a mathematical model that would establish a score of female representation per film based on the passiveness of female character and their relationship to the male roles in this film. 
>

> ### Do the main subjects change with time?
> 1. We first analyse the evolution of ratio of women to men over time. We can also carry this analysis with the crew members.
> 2. We look at the evolution of the importance of women in movies by analysing the score established in the previous part through time.
> 3. Finally and optionally, the results of the analysis are compared to social progress in the world of work in general to conclude on a possible correlation.

## Proposed timeline :clock10:
* 03/11/2022 Advanced definiton of our projects and reasearch questions
* 04/11/2022 Breakdown of the work and first analysis
* 11/11/2022 Merging of the different work to establish working dataset
* 15/11/2022 Brainstorming on better description of our project
* 16/11/2022 Integration of the different analysis & final redaction of the readme
* 18/11/2022 **Milestone P2**
* 25/11/2022 Brainstorm for the datastory
* 02/12/2022 **Homework 2 deadline**
* 09/12/2022 Perform final analysis and start datastory draft
* 16/12/2022 Complete the merging of the different parts and first final version of the datastory
* 20/12/2022 Last proofreading of the datastory and analysis workbook
* 23/12/2022 **Milestone P3**

## Team Organization :raised_hands:
<!---
A list of internal milestones up until project Milestone 3.
--->
<table class="tg" style="undefined;table-layout: fixed; width: 342px">
<colgroup>
<col style="width: 164px">
<col style="width: 178px">
</colgroup>
<thead>
  <tr>
    <th class="tg-0lax"></th>
    <th class="tg-0lax">Tasks</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">@marjoriecayatte</td>
    <td class="tg-0lax">General analysis on men/women differences<br><br>Code integration for Milestone P2<br><br>Readme proofreading</td>
  </tr>
  <tr>
    <td class="tg-0lax">@maximeleriche</td>
    <td class="tg-0lax">General analysis on movie countries<br><br>Dataset cleanup and completion regarding countries and regions<br><br>Code integration proofreading<br><br>Readme redaction & proofreading</td>
  </tr>
  <tr>
    <td class="tg-0lax">@madeleinerobert</td>
    <td class="tg-0lax">General analysis on movie box office<br><br>General analysis on movie score using IMDb dataset<br><br>Code integration proofreading<br><br>Readme proofreading</td>
  </tr>
  <tr>
    <td class="tg-0lax">@tuturta</td>
    <td class="tg-0lax">General analysis on movie genre<br><br>Gather of IMDb dataset<br><br>Code integration proofreading<br><br>Readme redaction & proofreading</td>
  </tr>
</tbody>
</table>

## Questions to TA :white_question:
- Do we have to analyse only one dataset or can we create a large dataset that we will reduce according to the analysis (because of missing value in some features) ?
- Is implementing a machine learning algorithm a requirement for the project ?

