# Is the cinema sexist ?


## Abstract :memo:
<!---
A 150 word description of the project idea and goals. What’s the motivation behind your project? What story would you like to tell, and why?)
--->
The CMU Movie Summary Corpus provides a collection of 42,306 movie plot summaries and metadata at both the movie level (including box office revenues, genre and date of release) and character level (including gender and estimated age). 
We aim to assess the evolution over time of the presence of women in the film industry. First, by focusing on the proportion and average age of actresses in the cast of a film, the study is then nuanced by looking at the characteristics of the characters played by these actresses using the Stanford CoreNLP-processed summaries. To deepen these results, the analysis is repeated first only on the most impactful films (number of votes on IMDB and box office revenue) and then, grouped by region of the world. 
Finally, the results of the analyzes are compared to social progress in the world of work in general to conclude on a possible correlation. (149/150 mots)

Ajout d'un schéma comme dans https://github.com/epfl-ada/ada-2021-project-acmu/blob/main/README.md ?
## Research Questions :grey_question:
<!---
A list of research questions you would like to address during the project.
--->
During the project we would like to adress these questions that could provide us with meaningfull insight into whether the cinema is sexist or not.

1. What is the ratio of women to men in cinema ? 
1. What is the impact of women in cinema?
1. Do these answers change over time and according to the region of the world considered?

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

Dire qu'elle hypothèse on a fait, quelle décision ex (se réduire à 5 genres) 

> ### What is the ratio of women to men in cinema ?
> 1. To start our investigation, we first explore ratio of women to men in cast overall, then by sorting by region or by gender. 
> 1. Then, we carry out the same analysis using the additionnal the crew database from IMDB.  
> 3. Finally, we will try to determine whether there is a correlation between the ratio of women in the film crew and in the film cast.
>
>Although the proportion of women in the industry can give us some good initial indicators as to the film industry's gender gap, it omits an even more important indicator. What is the representation of women in these films? Are they playing strong, impactful characters or are they playing roles dominated by men? 

> ### What is the impact of women in cinema?
> 1. As a first approach, we are interested in the representation of women in popular films, regarding both the box office revenue and number of votes on IMDB (from the additionnal dataset). Considering the IMDB score, the analysis continues by studying this time the representation of women in the well-received films.
>2. By working with the [Stanford CoreNLP-processed summaries](http://www.cs.cmu.edu/~ark/personas/), we expect to develop a mathematical model that would establish a score of female representation per film based on the passiveness of female character and their relationship to the male roles in this film. 
>

> ### Do the main subjects change with time?
Not only do politicians switch parties from time to time, but even opinions within the same party can fluctuate. Our first approach at monitoring quote trends involves counting the quotes containing a certain keyword by date and relating them to Google trends, to figure out whether they follow a similar pattern. The plot below suggests a link between the occurrence of "shooting" in Donald Trump's quotes and the search trend of the word. Furthermore, both can be related to mass shootings that happened in the US, such as the El Paso shooting, which corresponds to the highest spike in both trends.

<p align="center">
 <img src="./figures/trump_quotes.png" alt="trump quotes" width=500"/>
</p>
                                                                    
While examining approaches for answering our third research question, we discovered an important aspect of the dataset. Quotes may be referenced in news websites at a different time than originally spoken. Furthermore, news quotes may not be a direct representation of what politicians actually talk about. By definition, quotes are cherry-picked by authors that might be biased. For example, some websites are owned by politicians and controversial subjects are over-emphasised in the media.

<!---
> Can website biases influence our findings on the actual subjects politicians talk about?

Some subjects that may be important for a party are not highlighted in the media. 


(or synonyms of the word) 

 Initially, the analysis can be based on a list of pre-defined topics which we deem relevant to the speaker or party. We can implement an end-to-end approach by using the results of the sentence classifier in the first question to create a dynamic list of topics to look for.

* feasibility of the clusters 
* scaling the current analysis to multiple years
-->  
                                                                    


## Proposed timeline :clock10:
* 15.11.21 Integration of datasets for all years into current analysis.
* 19.11.21 Re-do clustering based on topics of interests.
* 22.11.21 Pause project work.
* 26.11.21 **Homework 2 deadline**
* 28.11.21 Perform final analyses.
* 08.12.21 Begin developing a rough draft of the datastory.
* 11.12.21 Complete all code implementations and visualisations relevant to analysis.
* 14.12.21 Complete datastory.
* 17.12.21 **Milestone 3 deadline**

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
    <td class="tg-0lax">@arinaraileanu</td>
    <td class="tg-0lax">Election prediction<br><br>Web development<br><br>Come up with meaningful visualizations<br><br>Continue exploring the dataset<br><br>Develop the final text for the data story</td>
  </tr>
  <tr>
    <td class="tg-0lax">@nitu-catalin1998</td>
    <td class="tg-0lax">Graph analysis over topics and parties.<br><br>Common words analysis<br><br>Develop the web interface<br><br>Analyze news website bias<br><br>Develop the final text for the data story</td>
  </tr>
  <tr>
    <td class="tg-0lax">@MihaiDavid05</td>
    <td class="tg-0lax">Graph analysis over topics and parties.<br><br>Topics analysis over time<br><br>Define topic of interests<br><br>Tune clustering<br><br>Develop the final text for the data story</td>
  </tr>
  <tr>
    <td class="tg-0lax">@umerhasan17</td>
    <td class="tg-0lax">Topics analysis over year<br><br>Develop the web interface<br><br>Integrate datasets of all years<br><br>Develop the final text for the data story</td>
  </tr>
</tbody>
</table>
