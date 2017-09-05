---
layout: post
title:  "NLP lecture to NYC Ascent post-docs"
date:   2016-02-28 21:39:00
categories: blog
---

Yesterday I had the pleasure to lecture, along with my colleagues Cesar Koirala and Ken Bame, about natural language processing and machine learning. We focused on three areas, with particular respect paid to natural language data: obtaining and processing, feature extraction, and machine learning.

The group to whom we lectured, [Ascent fellows](http://www.nycascent.org/), was interesting, being made up of science PhDs from Columbia, NYU, CUNY, and Cornell. The purpose of this group, by my understanding, is to give students of the hard sciences the tools they need – business, techincal, social – to succeed in the job market. This kind of grooming is very important, and equally rare, for those acclimated to culture of academia. As "digital humanities" (or whatever it will morph into) matures, a program like Ascent's could prove even more valuable for the success of post–PhD humanists. Since Ascent is funded by no less than the NSF, good arguments could be made for leading humanist–funding groups to sponsor something similar.

[Our GitHub notebook is available](https://github.com/kylepjohnson/lecture_nyc_ascent). The task we tacked was the prediction (binary classification, to be precise) of "viral" tweets. We made a collection of unpopular tweets (those with less the 10 RTs) and popular (over 500). Then, using nothing more than the text of the tweet, we explored (a) how many features we could extract and (b) how well various algorthms performed. To our pleasant surprise, using only a tweet's text, we came to an 84% precision and 85% recall (random forest and decision tree did equally well). Results would surely be improved were we to leverage two valuable feature sets – bag of words and topic modelling – however processing time on our local computers was too long for purposes of the class. Nevertheless, BOW and topic modeling code is included in the Jupyter notebooks should anyone want to give it a try. (I'll note that, from casual review of the data, unpopular tweets have higher occurences of profanity. For this reason, I think BOW especially would raise precision.)
