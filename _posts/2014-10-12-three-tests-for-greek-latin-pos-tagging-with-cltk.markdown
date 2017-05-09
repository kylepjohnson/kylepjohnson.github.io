---
layout: post
title:  "Three tests for Greek and Latin POS tagging with the CLTK"
date:   2014-10-12 20:59:00
categories: blog
---

*Important! This post contains incorrect accuracy scores. See <http://cltk.org/blog/2015/08/02/corrected-stats-pos-tagger-accuracy.html> for better information.*

I have been playing around with the NLTK's POS tagging, following along with Chapter 4 of <a href="www.amazon.com/Python-Text-Processing-NLTK-Cookbook/dp/1849513600/ref=sr_1_2">*Python Text Processing with NLTK 2.0 Cookbook*</a> by Jacob Perkins. (Note to self: Get the recently released <a href="www.amazon.com/Python-Text-Processing-NLTK-Cookbook/dp/1782167854/ref=sr_1_3">Python 3 Text Processing with NLTK 3 Cookbook</a>.) I have built POS training sets out of the data in the Perseus treebanks, which I am currently collecting in several CLTK repositories for <a href="https://github.com/cltk/greek_treebank_perseus">Greek</a> and <a href="https://github.com/cltk/latin_treebank_perseus">Latin</a>.

The following notebooks — <a href="http://kyle-p-johnson.com/notebooks/Unigram%20tagging%20of%20Greek%20and%20Latin%20with%20the%20CLTK.html">Unigram POS tagging</a>, <a href="http://kyle-p-johnson.com/notebooks/Bigram%20tagging%20of%20Greek%20and%20Latin%20with%20the%20CLTK.html">Bigram POS tagging</a>, and <a href="http://kyle-p-johnson.com/notebooks/Trigram%20tagging%20of%20Greek%20and%20Latin%20with%20the%20CLTK.html">Trigram POS tagging</a> — evaluate the accuracy of these algorithms combined with this training set. The `evaluate()` function runs your own tagger on the original training set, and then measures how accurate it was against the known–good values.

The results for this little experiment are:

<div class="panel panel-default">
  <!-- Default panel contents -->
  <div class="panel-heading">Greek and Latin tagger accuracy</div>
  <!-- Table -->
  <table class="table">
    <thead>
      <tr>
        <th>Tagger</th>
        <th>Greek</th>
        <th>Latin</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>UnigramTagger()</td>
        <td>0.9196123340065213</td>
        <td>0.8873793350017877</td>
      </tr>
      <tr>
        <td>BigramTagger()</td>
        <td>0.8125528866223641</td>
        <td>0.7211862333703404</td>
      </tr>
      <tr>
        <td>TrigramTagger()</td>
        <td>0.8101779247007322</td>
        <td>0.8162128596428504</td>
      </tr>
    </tbody>
  </table>
</div>

The Greek unigram and bigram taggers were more accurate than the Latin. Both of the Unigram taggers were significantly more accurate than the others. The most interesting discrepancy here is the Latin bigram tagger, which is 17% less accurate than the unigram and 10% less than the trigram. In always looking at one previous word, my tagger misinterprets ambiguous forms.

There are probably strengths to each of these taggers. The next step would be to include these in a backoff chain, like so:
{% highlight python %}
tagger = backoff_tagger(train_sents, [UnigramTagger, BigramTagger,
   TrigramTagger], backoff=backoff)
{% endhighlight %}
My next step to this will be to experiment with `backoff_tagger()`, varying the three taggers and their order.
