| **Average Revenue and Cost of Gacha Games**                |
|------------------------------------------------------------|
|   **Sydney Lieske, Isabella Morales, and Andrea Skvarova** |


## Abstract

This project takes data from different gacha games and is an analysis using R. We have an interest in gacha games and wanted to use this idea for our project. We found this data and decided to make comparisons between 4 different games. We had done some research on what we should do for this project and agreed that using R would be our main method. We wanted to look at Twitter data as well for this project. In R we scraped Twitter for tweets using the hashtag “\#GenshinImpact” or “Genshin Revenue”. We cleaned and found the top 15 unique words found in each type of tweet. We also found words that occur together the most in tweets. Lastly, we made a word network for tweets using these hashtags.

## Introduction

Being one of the largest franchises to come out in recent years, Genshin Impact has a large consumer base since 2020, making billions of dollars since release in order for customers to have more of a chance to have the chance to receive characters and weapons through Genshin Impact’s “gacha” system. It was a grand addition to the already long line of gacha games that are floating around the internet. For some, the game was their introduction to such games, for others, it was just another game to start playing. Our hope for this project is to investigate some of the top grossing gacha games around to see just how much money people spend on rare items or characters. We too have been ensnared in the world of spending money on video game characters and items but think it’s worth seeing what could be worth investing into when playing these games.

## Data

We have many sources of data due to a low amount of data sets pertaining to gacha games.

We wanted to make comparisons between the revenues of different games, so we chose 4 games to look at: Genshin Impact, AFK Arena, Raid: Shadow Legends, Fate/Grand Order.

Using a dataset from a fan create site called GenshinLab, we were able to see revenue per banner, which is the amount of money gained per 1 or 2 rare characters. We then gained a approximate number of downloads and revenue for the games we focused on from the site AppMagic. We found the numbers for the past 30 days and in its lifetime. The lifetime is defined as how long the game has been live or been in use.

Due to limited data on other games, we decided to primary focus on Genshin Impact data, working with datasets, as well as doing a sentiment analysis on tweets pertaining to the game because we found that it would be interesting to see what users had to say on the matter due to the size of the fanbase and also because our team has a genuine interest in this data, making it much more motivating to analyze the information we obtain over the course of this project.

For the Twitter Data, we used Twitter’s API and the R package “rtweet” to search for keywords and hashtags “Genshin Impact”, “Genshin Revenue”, and “Gacha Games” for this project. We took 5000 English tweets for each one to analyze.

To see how each character in Genshin Impact could possibly stack up against each other, we used the website paimon.moe, a fan made website that many players use to keep track of their transactions made in-game for each banner. They also have the information public to users, which made it much more helpful for us to understand how the revenue could have stacked up, especially when Genshin Impact introduced banners with two characters.

## Methods

**Why do you use this method?**

We wanted to see how much people spend on their favorite “gacha” games on hard-to-obtain content​. To do that, we first need to see how much they make in both the past 30 days and in its lifetime. We did research into all the games as well as pulling datasets from a fan made sites.

For the Tweet analysis, we used this method as it was easiest for us to use within R. We researched about different packages and methods for this and found this the most reproducible for us. With the use of a Twitter Developer account, we were able to scrap live tweets and clean the data for use.

**How do you apply this method?**

Using the method of pulling data from fan made sites was the only way we were able to find any concrete data for the project. Unfortunately, most datasets online pertain to character or weapon statistics on finding what is the best character or weapon, rather than revenue based. If there was one found, it was the same as what we already decided to do. We compiled all the relevant information in different excel books so we could create charts that could showcase differences.

This method for twitter mining was applied by first connecting to the Twitter API using a direct default authentication. Then the search_tweets function was used to search for “\#GenshinImpact”, “Genshin Revenue”, and “Gacha Games”, with 5000 tweets in English. Once those tweets were obtained in a csv file, the http elements needed to be removed, which was done manually. A list of words that are recognized as unique by R was created. The rest of the data was cleaned, the punctuation was removed, text was converted to lowercase, and each ID was added for each tweet. Stop words were then applied to remove them from the list of words. There were 3 plots created for each type of tweet subject, we found the count of the top 15 words found in the tweets. We then wanted to see which words occurred together the most in tweets. Using the devtools and widyr library in R, we found the paired words for each tweet subject. We then set up the data by separating the words and paired words to create a count for a word network. Lastly, we created word clouds for the tweets using the wordcloud and RColorBrewer packages.

## Results and Limitations

To understand how significant the differences in numbers are, Fate/Grand Order was released in July of 2015, Raid: Shadow Legends in July of 2018, AFK Arena in April of 2019, and Genshin Impact in September of 2020. Fate/Grand Order has a noteworthy lead on all games as it came out before any of them, making \$6.3B since release. You would think that the next highest grossing would be the next oldest, but surprisingly it is the youngest game, Genshin. Making \$3.7B in just 2 years. Third, is AFK Arena making \$1.45B, and lastly is Raid: Shadow Legends making \$247M. It shows just how much more popular Genshin Impact is compared to other gacha games. Even moreso, as seen in Figure 11, the amount of revenue made in the past 30 days gives Genshin a substantial lead over the others. They made more than \$100M in comparison to the measly \$5M AFK Arena made.

With the Twitter analysis done for this project, we had found that under the \#GenshinImpact tag on Twitter, in Figure 1 the top 3 words tweeted, that aren’t “genshin impact”, were “scaramouche”, “wanderer”, and “fanart”. This is a very popular character in the game currently and with loads of artists creating fanart for them. With scaramouche being the most recent and popular banner character to come out, it was expected that it would be in the top. The top 3 words found in “Genshin Revenue” that were unique, in Figure 2 were “Game”, “Sonic”, and “billion”. It was interesting to see that “Sonic” was in the top tweets, but that it because both games were up for the Player’s Voice award, with Genshin winning the category. In in figure 3 the last topic “Gacha Games” was found to have “play”, “money”, and genshin” as the top 3 words. As Genshin Impact is one of the top franchises for gacha games it was expected for it to be in the top 3 along with money as the premise for gacha games is for players to spend in-game currency for virtual items.

In Figure 4, the most occurred paired words found with “\#GenshinImpact” was “Genshin Impact” at 387 tweets, and the next unique occurrence was “happy birthday” at 267, and “mommy sorry” at 212. As expected the game franchise is the most tweeted, followed by “happy birthday” as the character “Nilou” recently celebrated their birthday in game, and “mommy sorry” as Genshin Impact fans have a strong interest in the mother character and their popularity. Figure 5, the word network created using the hashtag “\#GenshinImpact” it was found that the most popular characters, and recent, were the most tweeted about within this tag.

In the Figures 6-8, these are the word clouds for each topic.

For “\#GenshinImpact”, it was seen that “scaramouche”, “wanderer”, and some other popular characters were the most important of each tag. Scaramouche also known as “wanderer” was the most recent and popular character released in this game. For “Genshin Revenue”, the most relevant important words featured are, “sonic”, “billion”, “mobile”, and “money”. For “Gacha Games”, the most important words that stand out are “play” and “game”.

Some limitations and issues that were occurring in this analysis were irrelevant or repeating words appearing many times. This made the data a bit more difficult to work with but still gave us a good insight on which words were the most tweeted. As well as it is taking data from Twitter, a reoccurring issue was one specific user tweeting an enormous amount, to the point that they showed up as the most tweeted under a specific tag.

When looking at Figure 9, we can see the overall revenue of each patch made since release on iOs in China. The highest earning point of the game’s entire lifespan would have to be patch 2.6, which featured the release of highly anticipated Kamisato Ayato with Venti, followed by Kamisato Ayaka who is one of the most popular characters in game. Another factor that led to this high revenue is due to China being under a strict covid lockdown at the time, keeping the banner up for much longer.

The next highest earning banner being version 1.0, when the game first released and hype for the game was at its highest. The banner with the lowest revenue was for version 1.6, which featured Klee rerunning, however losing popularity due to her strength and clunky gameplay, and Kaedehara Kazuha, a character whose full potential wasn’t yet released, as we can discuss later. Not only that, but the second major update to the game, version 2.0, was coming right after this patch, which led to people saving for whoever comes from that new region.

With Figure 12, we are able to see the cumulative number of summons made per character in Genshin Impact. Taking the user submitted data from paimon.moe and compiling it into an excel sheet by hand, we took each character’s time shown up for each banner and put it into one chart. From this, we can see which characters were most interesting for players that shared their results. The most summoned character in Genshin Impact would be Raiden Shogun, a character who is a ruler over a region in the game, a character that many players consider to be strong, along with being considered attractive, as seen in the sentiment analysis done earlier. The second character to be wished the most would be Kaedehara Kazuha, a genuine surprise when looking at his first release but making more sense in the long run due to his return banner of 2.8 performing well, alongside the fact that when he shows up, he is partnered alongside some of the lesser popular characters, Klee and Yoimiya in which he takes most of the banner revenue.

The least wished for characters in Genshin impact are Tighnari, Nilou, and Cyno. This can mostly account to the fact that these characters are very new to the game, meaning they have not had a second banner to show up in. Tighnari was one that was destined to not perform well due to his inclusion into the standard banner, which will always be around. However, Klee was the next lowest character after all of these which is interesting since she is one of the oldest characters in game, showing up multiple times, however she cannot perform as well as later characters to release who have kits that can outperform her easily.

## Future Study

When looking back, there are some issues that we ran into when working on our research. The first one being that some of the data might not align due to where they were sourced. With revenue overall, we gathered it specifically from China’s iOS market compared to overall pulls being sourced from a generally western audience. An issue that can be found in that is how different the audiences are interested in things as general marketing knows that that different groups of people react differently to certain things. Genshin Impact’s characters are made to cater to different people and playstyles, so where one character might be favored in one region might be strongly disliked in the other, though we do not have the data for that.

## References

![Chart Description automatically generated with medium confidence](media/ab54f2a2308b70e8e11a8f4d40613f0b.png)Figure 1: Top 3 unique words in tweets using the hashtag - \#GenshinImpact

![Chart Description automatically generated](media/b966c2a69fef925f7a51af0d306c4a49.png)Figure 2: Top 3 unique words in tweets using “Genshin Revenue”

![A picture containing table Description automatically generated](media/0dc3ff49d619f39eafdce8cc7bd0dccb.png)Figure 3: Top 3 unique words in tweets using “Gacha Games”

![Graphical user interface, text, application, email Description automatically generated](media/290df57b2824b3715e27b34c13d02c5e.png)

Figure 4: Most common paired words within \#GenshinImpact

![Chart, scatter chart Description automatically generated](media/f5eb00497456657c551d4dcd149d6993.png)Figure 5 Word Network: Tweets using the hashtag \#GenshinImpact

![Text Description automatically generated](media/fd7abff8d786e1e724cfe69cec834e6f.png)Figure 6: WordCloud for \#GenshinImpact

![Text Description automatically generated](media/89bf0e67ece218ea3ebfa1b468d2dc16.png)Figure 7: WordCloud for “Genshin Revenue”

![Text, whiteboard Description automatically generated](media/ae7bdd5718764c19f345fc1bdb143175.png)Figure 8: WordCloud for “Gacha Games”

![Chart, bar chart, histogram Description automatically generated](media/f31b7874b66a248474d51a05c9109a4c.png)

Figure 9: Sum of Revenue by Version

![](media/43e17b4859b041ff21ff86b6c6148b1e.png)

Figure 10: Lifetime Revenue of gacha game

![](media/32a7c2b28c3f90ba16a2a0d9d85d2c87.png)

Figure 11: \~ Revenue made in past 30 days

![Chart Description automatically generated](media/08d2cf188c547b8565923f19dededfd2.png)

Figure 12: Cumulative amount summoned per character in Genshin Impact
