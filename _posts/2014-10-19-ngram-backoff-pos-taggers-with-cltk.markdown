---
layout: post
title:  "N–gram backoff POS tagging with the CLTK"
date:   2014-10-19 10:36:00
categories: blog
---

*Important! This post contains incorrect accuracy scores. See <http://cltk.org/blog/2015/08/02/corrected-stats-pos-tagger-accuracy.html> for better information.*

Since <a href="/blog/2014/10/12/three-tests-for-greek-latin-pos-tagging-with-cltk.html">my last post on n–gram part–of–speech taggers for Ancient Greek and Classical Latin</a>, I have been working on integrating these taggers and datasets into the core of the CTLK. With this finished (<a href="http://docs.cltk.org/en/latest/index.html">see docs</a>), I am returning to continue to test the quality of these POS taggers and to develop better ones.

In brief, I have found that the quality of the taggers is dramatically improved when combining them together in a backoff chain. For those who are not familiar, backoff tagging is combining the unique powers of each tagger in order to build an algorithm which makes the best possible decisions.

>**Backoff tagging** is one of the core features of `SequentialBackoffTagger`. It allows you to chain taggers together so that if one tagger doesn't know how to tag a word, it can pass the word on to the next backoff tagger. If that one can't do it, it can pass the word on to the next backoff tagger, and so on until there are no backoff taggers left to check. (Perkins, *Python Text Processing with NLTK 2.0 Cookbook*, 88)

For an illustration of the power of this technique, I offer two of my latest iPython notebooks, on <a href="/notebooks/N-gram%20backoff%20tagging,%20Greek.html">Greek</a> and <a href="/notebooks/N-gram backoff tagging, Latin.html">Latin</a> n–gram POS tagging. Whereas for Greek, by themselves the taggers had an accuracy of 92% at best and 81% at worst, and 89% and 72% respectively for Latin, when used in a chain the accuracy soared for both languages (97% and 98%).

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
    </tbody>
  </table>
</div>

These results are exciting for several reasons. First and foremost, a 97%+ accuracy rate is simply very high. As a contrast, when using the same backoff chain for the English language (in fact, a slightly better one), using the NLTK's training sets, Perkins gets 88%. A second reason for enthusiasm is that these results will make it all the easier for <a href="https://en.wikipedia.org/wiki/Supervised_learning">*supervised learning*</a>, that is using human POS checkers to manually edit newly machine–tagged text. Thus, we can use the CLTK to tag texts which are not part of the current training set, then correct their ~2-3% errors, and finally add them back to an expanded and improved training set.

Despite these promising results, the work to expertly machine–tag POS with the CLTK is just beginning. My next steps will be to continue to explore the NLTK's tagging trainers. I am especially hopeful for `RegexpTagger()` (94–86), `AffixTagger()` (96–97), and `BrillTagger()` (98–100), the first two being especially well suited for highly inflected languages.

And despite improvements to come, I think it is time to begin reaching out to language educators, whom I hope will be able to bring the CLTK to the classroom. Beginning students of Greek and Latin (say, second through third years) are perfect candidates for contributors for this supervised learning, as their first central challenge is to precisely decode parts–of–speech. I am beginning to reach out to my contacts who have expressed interest in using POS tagged texts in their Ancient Greek and Latin courses.

