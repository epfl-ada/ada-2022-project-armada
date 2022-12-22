# Cinema: a patriarchal industry?

The cinema industry has a long and complex history when it comes to the representation and portrayal of women on screen. From the earliest days of film, women have often been relegated to supporting roles or objectified as props for male characters. Despite some notable exceptions, the industry has historically been dominated by men, both behind and in front of the camera.

In this article, we will explore the place of women in the cinema industry through the lens of data from the CMU Movie Summary Corpus, and additional data from the ImdB API.

We will explore the situation of women in the movie industry since the beginning of the 20th century. Is their an evolution across countries or movie genre?

Men and women might be portrayed differently on the movies. Is there an objectification of women? What about men?

We will finally investigate how men compare to women in terms of careers in the cinema industry. Is there a noticeable difference in how movies featuring them are perceived?

## Quick glance at the dataset

- ratio h/f
- plage temporelle
- nombre films
- nombre total de votes sur IMDb

## So few women?

### A look at the film industry by continent

Gender equality is not uniform across the globe, is this reflected in the cinema industry as well?

Our dataset contains % (nb_men - nb_women / nb_women) more men than women, but is this a common feature across the globe?

[Bar plot]

It appears that the disparities in women share is a constant independent of the region studied. Maybe averaging over all periods of time hides an era with a different tendency.

[interactive PLOT with ratio by region]

Despite looking more precisely at a year level, men remained predominant over women in every region, this since early 20th century.

Classifying movies by region does not highlight an ounce of equality when it comes to women place in the cinema. However another natural classification can be done over their genre.

### A gender analysis of movie genres

Look at these posters of action movies, no women to be found!

[POSTER 4-5 films]

Let's analyse the representation of women in specific movie genres and see whether some have more or less gender balance in terms of characters.

We will focus on the main genres in the film industry, including comedy, romance, thriller, drama, and action.

[PLOT with ratio par movie genre]

As expected, romance movies star more women than action movies, but the general trend remains the same: men still are predominant in the casting.

It is not enough to simply look at the number of men and women in the industry to accurately assess the role of women in the industry. We must also consider the quality of their representation, which can be determined by examining the types of characters they portray and whether or not they are given leading roles. By exploring these factors, we can gain a better understanding of how gender is portrayed in the industry.

## The archetypical role

Let's create a report on the typical male and female character archetypes, including few features such as their ages or heights, and which adjectives are used to qualify them.

[Cloud of word]

*The dataset used to gather the adjectives was created by the paper Learning Latent Personas of Film Characters given in the CMU dataset. It classifies 501 characters into 72 character types, which is way smaller than the other dataset used, therefore the result has to be taken with a pinch of salt.*

As we can see, women are mostly described by their physical traits (blonde, beauty) however the intellectual features are not glorifying (dumb, brainless).

On the contrary, the typical male character is depicted as the hero (hero, hunter, father etc.) with more interesting and complex features (jealous, corporate, crazy, corrupt).

This comparison highlights a clear materialization of women in the cinema, which is not the case for men who have roles with more depth. In addition women tend to be younger, perhaps to star better-looking actresses.

Knowing women are attributed a more simplistic role than man, does it necessarily mean that they are secondary actresses?

We analyzed the plot summary data in the dataset and searched for character names to determine how likely an actress is to be a main character, and same for actors.

[% de chances d'etre acteur principal homme/femme]

[Analyse a faire]

To evaluate the differences between men and women, this analysis of the representation of the actor/actress through the character may not be enough. Specifically it does not convey how the movie is received by the public, and whether the actors manage to build a career.

## Famous as a woman?

### Movie popularity and quality
A natural metrics to assess the success of a movie is its rating by the public on IMDb. Let's check if the average movie rating of a given actor differs on its gender.

[GRAPH]

As we can see, both gender obtain an average movie rating of 6.1, and the distributions are about the same.
Thus the quality of the filmography is independent of the gender, but another interesting point of view is the movie popularity.

To check this, we analyse the women ratio in regards to the number of votes.

[Graph heat map]

The general trend is that the higher the number of votes, the smaller the female ratio is.

In addition, there is no movie with more than one million votes and with a ratio higher than 50% despite the fact some movies are rated more than two million times.

A possible explanation could be that highly popular movies are action movies, which as we saw have the smallest female ratio.

Women seem not to be a factor for a movie popularity, does it mean they cannot build a proper career?

### Career

An available data to us is how many movies an actor played in. We base the quality of a career on that feature.

[GRAPH]

Look at how many movies a single actor can play in, up to 200!
However it is not the case for all actors... actresses only reach up to 100 movies.

This difference highlights a general trend: the average career of an actress is 40-movie long, whereas actors play in average in 65 movies.

## IV. Conclusion

Time to come back to our initial question: is the cinema a patriarchal industry?

Our results highlight different phenomena:

- The industry portray less women than men regardless of the country, the movie genre, and the time period.
- Women have less significant role, [à completer] 
- Women build smaller careers, and appear in less popular movies.

While these results suggest that the industry is patriarchal, some indicators show that there is a degree of equality as well. Indeed movie ratings, and chance of being the lead actor seems to be gender independent.

However the movie industry is a complex machine, and includes many other factors than the one we have in the dataset (casting selection, crewmembers, etc.).

Another bias regarding the data comes from the choice of the movie made beforehand as there could have been a prior selection based on hidden covariates.

Our work can be completed with other analysis, such as [Article NATURE] which uses the dialogs to implement a Bechdel test.