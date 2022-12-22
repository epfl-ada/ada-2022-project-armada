# Cinema: a patriarchal industry?
[Datastory webpage](https://epfl-ada.github.io/ada-2022-project-armada/)
## Abstract :memo:
<!---
A 150 word description of the project idea and goals. What’s the motivation behind your project? What story would you like to tell, and why?)
--->
The CMU Movie Summary Corpus provides a collection of 42,306 movie plot summaries and metadata at both the movie level (including box office revenue, genre and date of release) and the character level (including gender and estimated age). 
Our goal is to assess women place in the movie industry given different period of time, region, or movie genre. In addition we will examine how the average character is depicted depending on its gender, and finally analyse whether careers and ratings are influenced this factor.

## Research Questions :grey_question:
<!---
A list of research questions you would like to address during the project.
--->
During the project we would like to adress the following questions in order to answer to our problematic:

1. Are women under respresented in the cinema industry? What is the situation and how has it evolved over time and region?
2. How are characters represented? Have the traditional depictions of women characters in the industry changed?
3. Does gender impacts either the success of a movie or the career of the actor?

<a name="additional-datasets"></a>
## Additional Datasets :fax:
<!---
List the additional dataset(s) you want to use (if any), and some ideas on how you expect to get, manage, process, and enrich it/them.
Show us that you’ve read the docs and some examples, and that you have a clear idea on what to expect. Discuss data size and format if relevant.
It is your responsibility to check that what you propose is feasible.
--->
To deepen the analysis and recover the missing values, we use the following additionnal datasets:

* [Country API](https://restcountries.com/): List countries by world region in order to get region for each movie in the database where country is reported. We can therefore conduct an analysis based on region.

* [title.ratings](https://www.imdb.com/interfaces/): provides **IMDb average rating** and **number of votes** for more than a million of movies and series. This additionnal information allows us to quantify the success and the popularity of a movie and then complete the information provided by the box office revenue in the Freebase Movie dataset which contains around 90% of missing values. 

The link between the **Freebase movie ID** with the **IMDb movie ID** (*tconst*) is made using 3 matching criteria: `Movie Name`, `Movie Release Date` and `Movie Runtime`. This brings us to about 45,000 matches out of 80,000 films in the Freebase database.

## Methods :mag:

**<span style="color:green">not precise enough
*check or specify that there is a bias coming from the data</span>**
After our first analyses of the data, we chose to make some hypotheses for our futur work :

- The datasets provided have been extracted in 2012 from Freebase, thus we will only consider movies until 2012 and not the few movies that have release dates between 2013 and 2016.
- We will only consider these five principal movie genre: drama, comedy, romance, action and thriller. "Black and white" is listed as a genre in the dataset and is the forth most represented one but we chose not to consider it. Indeed, it does not seem to be a genre that will be meaningful for our analysis on the impact of women in cinema.

> ### What is the ratio of women to men in cinema ?
> 1. To start our investigation, we first explore ratio of women to men in overall cast, then by sorting by region or by genre. 
> 2. Then, we carry out the same analysis using the additionnal crew database from IMDb.  
> 3. Finally, we will try to determine whether there is a correlation between the ratio of women in the film crew and in the film cast.
>
>Although the proportion of women in the industry can give us some good initial indicators as to the film industry gender gap, it omits an even more important indicator. What is the representation of women in these movies? Are they playing strong, impactful characters or are they playing roles dominated by men? 

> ### What is the impact of women in cinema?
> 1. As a first approach, we are interested in the representation of women in popular films, regarding both the box office revenue and number of votes on IMDb (from the additionnal dataset). Considering the IMDb score, we continue the analysis continues by studying this time the representation of women in the well-received films. **<span style="color:green">you need to precise steps to come to conclusion</span>**
> 2. By working with the [Stanford CoreNLP-processed summaries](http://www.cs.cmu.edu/~ark/personas/), we expect to develop a mathematical model **<span style="color:green">ywhich one, what data, which form? </span>** that would establish a score of female representation per movie based on the passiveness of female characters *how is it measured?* and their relationship to the male roles in this movie. 
>

> ### Do the main subjects evolve over time?
> 1. We first analyze the evolution of ratio of women to men over time. We can also carry this analysis with the crew members.
> 2. We look at the evolution of the importance of women in movies by studying the score established in the previous part through time.
> 3. Finally and optionally, the results of the analysis are compared to other parameters of gender gap (number of working women for example) to conclude on a potential correlation. **<span style="color:green">how? what can you conclude? </span>**
> 
## Proposed timeline :clock10:
* **03/11/2022** Detailed choice of our project and determination of reasearch questions
* **04/11/2022** Breakdown of the work into individual tasks and first analyses
* **11/11/2022** Merging of the different works to establish working dataset
* **15/11/2022** Brainstorming on clearer description of our project
* **16/11/2022** Integration of the different analyses & final redaction of the readme
* **18/11/2022** **<span style="color:red">Milestone P2</span>**
* **25/11/2022** Brainstorm for the datastory
* **02/12/2022** **<span style="color:red">Homework 2 deadline</span>**
* **09/12/2022** Perform final analysis and start datastory draft
* **16/12/2022** Complete the merging of the different parts and first final version of the datastory
* **20/12/2022** Last proofreading of the datastory and analysis workbook
* **23/12/2022** **<span style="color:red">Milestone P3</span>**


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
    <td class="tg-0lax">General analysis on men/women differences (age/height)<br><br>Code integration for Milestone P2<br><br>Readme proofreading</td>
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

## Questions to TA :grey_question:
- Do we have to work on only one dataset or can we create a large dataset that we will reduce according to the analysis (because of missing value in some features) ?
- Is implementing a machine learning algorithm a requirement for the project ?
- Does the majority of our results should be extracted from the main dataset (CMU) ?

