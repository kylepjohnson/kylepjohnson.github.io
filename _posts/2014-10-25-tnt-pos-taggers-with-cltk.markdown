---
layout: post
title:  "TnT POS tagging with the CLTK"
date:   2014-10-25 10:36:00
categories: blog
---

*Important! This post contains incorrect accuracy scores. See <http://cltk.org/blog/2015/08/02/corrected-stats-pos-tagger-accuracy.html> for better information.*

<a href="/blog/2014/10/19/ngram-backoff-pos-taggers-with-cltk.html">My previous post built on the CLTK's n–gram taggers</a> and used them in conjunction with each other. Now I am considering a TnT tagger which I have created, whose results are even more promising than the backoff tagger. My detailed notes are available in <a href="/notebooks">/notebooks</a>.

Before diving into what a TnT tagger does, here are its results, along with those from my previous experiments.

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
        <td>1–gram > 2–gram > 3–gram</td>
        <td>0.972572292486997</td>
        <td>0.9796586568315676</td>
      </tr>
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
      <tr>
        <td>TnTTagger()</td>
        <td>?</td>
        <td>0.9871855183184991</td>
      </tr>
    </tbody>
  </table>
</div>
Judging by the Latin example, these results are very promising. The tagger works for Greek, though `evaluate()` does not finish running after almost 10 hours on my personal computer (a fairly new MacBook), so I will need to borrow time on something more powerful.

"TnT" is short for "Trigrams'n'Tags". Its strength over n–gram taggers used in a backoff is that the TnT tagger evaluates the probability of a tag among all three n–gram options, not just one at a time. The results of this tagger speak for themselves, though it will fail on unknown words. In continuing my work I plan on creating affix taggers for each language, which will read the tags of morphological beginnings and endings, and then pass this as a special tagger for unknown words with, e.g., `tnt.TnT(unk=suffix_tagger, Trained=True)`. In doing so, I will be following the lead of the TnT's creator, whose <a href="http://www.coli.uni-saarland.de/~thorsten/publications/Brants-ANLP00.pdf">initial research, available as a .pdf here</a>. For more on the NLTK's tagger, see also pp. 100–102 of Perkins's, *Python Text Processing* and of course <a href="http://www.nltk.org/api/nltk.tag.html#module-nltk.tag.tnt">the NLTK's API docs</a>.
