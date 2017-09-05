---
layout: post
title:  "CLTK POS tagging cross–validation"
date:   2014-12-31 20:02:00
categories: blog
---

*Important! This post contains incorrect accuracy scores. See <http://cltk.org/blog/2015/08/02/corrected-stats-pos-tagger-accuracy.html> for better information.*

A few months ago, I began a series of blog posts which reported on the CLTK's in–progress POS taggers ([the most recent here](http://kyle-p-johnson.com/blog/2014/10/27/affix-pos-tagging-with-cltk.html)). In these, I gave simple evaulations of the taggers which are now part of the CLTK's core. Now, I would like to offer a sounder evaulation of the taggers' accuracy.

Earlier, I simply tested the tagger against the entirety of the training set with which the tagger was made. This was computationally burdensome and, as I have recently learned, not the best the way to test the accuracy of my models. While reading Peter Flach's [*Machine Learning*](http://www.amazon.com/Machine-Learning-Science-Algorithms-Sense/dp/1107422221/ref=sr_1_1) (Cambridge 2012), I came across the following recipe for cross-validation, which is useful for checking a model for overfitting[¹](#1) (something I have been concerned with the complex Ancient Greek and Latin corpora).

> If overfitting occurs, the test set performance will be considerably lower than the training set performance. However, even if we select the test instances randomly from the data, every once in a while we may get lucky, if most of the test instances are similar to training instances – or unlucky, if the test instances happen to be very non–typical or noisy. In practice this train–test split is therefore repeated in a process called *cross–validation* …. This works as follows: we randomly divide the data in ten parts of equal size, and use nine parts for training and one part for testing. We do this ten times, using each part once for testing. At the end, we compute the average test set performance (and usually also its standard deviation, which is useful to determine whether small differences in average performance of different learning algorithms are meaningful). Cross–validation can also be applied to other supervised learning problems, but unsupervised learning models typically need to be evaluated differently. (p. 19; see also p. 349-350)

Because the treebank data from Perseus comes in large blocks of an author's text, I first randomized the tagged sentences, then chunked the text into ten parts, and finally built each of the models ten times in succession, reserving a different chunk for the test set each time. The code for this testing is all in [Cross-validation of the CLTK's POS taggers, Latin](http://kyle-p-johnson.com/notebooks/Cross-validation of the CLTK's POS taggers, Latin.html) and [Cross-validation of the CLTK's POS taggers, Greek](http://kyle-p-johnson.com/notebooks/Cross-validation of the CLTK's POS taggers, Greek.html)

For the ten passes for each algorithm, I took the average and standard deviation. Note that I am leaving out of this table to the affix taggers, which performed poorly (sometimes less that 10% accuracy).

<div class="panel panel-default">
  <!-- Default panel contents -->
  <div class="panel-heading"> Latin tagger accuracy</div>
  <!-- Table -->
  <table class="table">
    <thead>
      <tr>
      	<th></th>
        <th>Unigram</th>
        <th>Bigram</th>
        <th>Trigram</th>
        <th>Backoff</th>
        <th>TnT</th>
      </tr>
    </thead>
    <tbody>
      <tr>
      	<td>avg</td>
        <td>0.851957</td>
        <td>0.607023</td>
        <td>0.690828</td>
        <td>0.942375</td>
        <td>0.951578</td>
      </tr>
      <tr>
      	<td>stdev</td>
        <td>0.005064</td>
        <td>0.018504</td>
        <td>0.028856</td>
        <td>0.006851</td>
        <td>0.005047</td>
      </tr>
    </tbody>
  </table>
</div>

As we saw before, the TnT tagger is the the leader, with my custom 1-, 2-, 3-gram backoff tagger a close second. In favor of the latter, perhaps, the backoff tagger is considerably faster to build. To my pleasure, both perform at accuracies at or above what is expected from English language taggers (see Chapter 4 of Perkins's *Python Text Processing* for statistics).

The results for Greek are remarkably similar to the Latin, in both the best taggers, again the backoff and TnT, and their accuracy.

<div class="panel panel-default">
  <!-- Default panel contents -->
  <div class="panel-heading"> Greek tagger accuracy</div>
  <!-- Table -->
  <table class="table">
    <thead>
      <tr>
      	<th></th>
        <th>Unigram</th>
        <th>Bigram</th>
        <th>Trigram</th>
        <th>Backoff</th>
        <th>TnT</th>
      </tr>
    </thead>
    <tbody>
      <tr>
      	<td>avg</td>
        <td>0.905164</td>
        <td>0.736676</td>
        <td>0.725990</td>
        <td>0.952938</td>
        <td>0.954957</td>
      </tr>
      <tr>
      	<td>stdev</td>
        <td>0.001851</td>
        <td>0.007628</td>
        <td>0.008456</td>
        <td>0.002399</td>
        <td>0.001321</td>
      </tr>
    </tbody>
  </table>
</div>

Though I plan on analyzing the ~5% error (especially the types of words they currently fail), the slight standard deviation here, about half a percent for these two best taggers, tells me that these are not getting caught up in the specificity of any one set of trianing texts, that is are not overfit.


### Notes
<div id="1">1.</div>A succinct explanation of overfitting: 'The possibility of overfitting exists because the criterion used for training the model is not the same as the criterion used to judge the efficacy of a model. … Overfitting occurs when a model begins to "memorize" training data rather than "learning" to generalize from trend.' ([Wikipedia](https://en.wikipedia.org/wiki/Overfitting))
