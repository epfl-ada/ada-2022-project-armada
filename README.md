# Cinema: a patriarchal industry?
[Datastory webpage](https://armada.teleporthq.app/)
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

> ### Are women under respresented in the cinema industry? What is the situation and how has it evolved over time and region?
> 1. We complete the data with the movie region of origin, and sort all movies by region, and then by genre.
> 2. We compute the female ratio on the actor, and create graphs to visualize how present women are depending on these factors.

> ### How are characters represented? Have the traditional depictions of women characters in the industry changed?
> 1. We first use the tvtropes dataset to get the adjective that qualify a set of characters, and get a set of adjective for men and women.
> 2. We compute the average height and age of actors depending on the gender.
> 3. We check which characters name appear at least once in a plot summary,[Arthur partie pour expliquer les chiffres qu'on a]

> ### Does gender impacts either the success of a movie or the career of the actor?
> 1. We use the IMDb dataset to get the average rating of each movie, and for each gender look at the distribution of actor per average movie rating
> 2. We compute the female ratio depending on the number of votes on the movie
> 3. Build the CCDF of the amaount of movies per actor, depending on the gender
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

