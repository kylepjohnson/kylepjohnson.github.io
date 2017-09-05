---
layout: post
title:  "Tf-idf pairwise similarity in the Latin canon"
date:   2015-02-01 23:45:00
categories: blog
---

Several weeks ago a journalist asked me some interesting questions about [tf-idf](https://en.wikipedia.org/wiki/Tf%E2%80%93idf), which got me thinking about related tasks for, what else, the Latin and Greek authors of the PHI5 and TLG corpora. In these initial attempts, I have decided to offer a survey of *pairwise similarity*, which essentially takes two documents and returns a score of how similar the two are to one another. I won't try to explain the mathematics of how this works (because I cannot very well), though [this StackOverflow answer is as friendly as I've seen](http://stackoverflow.com/a/6255993).
>Tf-idf is a transformation you apply to texts to get two real-valued vectors. You can then obtain the cosine similarity of any pair of vectors by taking their dot product and dividing that by the product of their norms.

With an IPython notebook ('[Tf-idf pairwise similarity, Latin](/notebooks/Tf-idf pairwise similarity, Latin.html)'), I have generated a 7.7MB [file of all possible tf-idf pairwise similarity comparisons for the Classical Latin canon](/assets/phi5_tfidf_pairwise_sims_final.tar.gz) (1.0MB compressed). In this, I have taken every author's (362 of them) file in the PHI5 and compared them to the the other 361 (plus to itself). So if we compare 362 documents to 362, we wind up with 131044 (= 362 * 362) scores. (Of course, half of these are duplicates, though I am keeping scikit's verbose output, which is useful for some modeling.)

Let's say we compare the similarity of Vergil to himself, we would get a score of '1.0' (see line 100552).
>'Publius Vergilius Maro, Virgil, Vergil v. Publius Vergilius Maro, Virgil, Vergil': '1.00000000',

This means that the two texts are identical in their tf-idf. But what about Vergil to, say, Lucretius (line 100616)?
>'Publius Vergilius Maro, Virgil, Vergil v. Titus Lucretius Carus': '0.69055837',

A 69% similarity. Not terribly shocking considering that they wrote in the same century and in the same meter. But how about Vergil's similarity to someone with whom we might expect fewer commonalities?
Turning to Varro, a contemporary who wrote prose technical treatises, we have 62% (line 81728).
>'Marcus Terentius Varro, Varro v. Publius Vergilius Maro, Virgil, Vergil': '0.62273357',

Some similarities there, too, clearly. How about to Julius Caesar (line 100379)?
>'Publius Vergilius Maro, Virgil, Vergil v. Gaius Iulius Caesar, Caesar': '0.58061057',

I am just scratching the surface here, so I hope others will dig into the data and share any interesting or unexpected divergences or convergences. Certainly we will find some shocking similiarities between texts which are typically assumed to be dissimilar. Once I have factored into the CLTK core PHI author and work indexing logic, I can compare all individual works to one another.

Next I plan on turning to the TLG, though I may need to find some heavier computing power. At 1823 author files, scikit will need to generate 3,323,329 comparisons. And if we break down author files into their individual works, at an average of 3 works per author, we're looking at a staggering 30,206,016 scores.

Thanks to everyone reading and encouraging my research. Please feel free to share any insights.