---
layout: post
title:  "Affix POS tagging with the CLTK"
date:   2014-10-27 10:36:00
categories: blog
---

*Important! This post contains incorrect accuracy scores. See <http://cltk.org/blog/2015/08/02/corrected-stats-pos-tagger-accuracy.html> for better information.*

Affix tagging looks at the beginning or ending of a word and chooses a POS tag. I've worked through a number of <a href="/notebooks/Affix%20tagging,%20Greek%20prefixes.html">prefixes</a> and <a href="/notebooks/Affix tagging, Greek suffixes.html">suffixes for Greek</a> and <a href="/notebooks/Affix%20tagging,%20Latin.html">Latin</a>. Combined with <a href="/blog/2014/10/25/tnt-pos-taggers-with-cltk.html">ongoing results from my previous post</a>, the affix tagger results are:

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
      <tr>
        <td>2-char prefix</td>
        <td>0.1399196687464037</td>
        <td>0.11491635775172647</td>
      </tr>
      <tr>
        <td>3-char prefix</td>
        <td>0.166630938815114</td>
        <td>0.15512861524565794</td>
      </tr>
      <tr>
        <td>4-char prefix</td>
        <td>0.16541243103584444</td>
        <td>0.16120655589635513</td>
      </tr>
      <tr>
        <td>2-char suffix</td>
        <td>0.20355849401464465</td>
        <td>0.22117682479348175</td>
      </tr>
      <tr>
        <td>3-char suffix</td>
        <td>0.2462203693883768</td>
        <td>0.2615772538245865</td>
      </tr>
      <tr>
        <td>4-char suffix</td>
        <td>0.23366014915437816</td>
        <td>0.2749374329638899</td>
      </tr>
      <tr>
        <td>5-char suffix</td>
        <td>0.18811560028431848</td>
        <td>0.2376041999887097</td>
      </tr>
      <tr>
        <td>6-char suffix</td>
        <td>0.1341543217537486</td>
        <td>0.1721957736672751</td>
      </tr>
    </tbody>
  </table>
</div>

Clearly these taggers, by themselves, are not as good as the others. Still, they surely have some good utility in highly inflected languages. Their value will be apparent, I suspect, when combined in a backoff chain with n–gram or other taggers.

But before doing extenisive tests of all of these taggers used in various backoff orders, I will be writing a proper noun dictionary for Greek and Latin, drawn from the TLG and PHI5 corpora. This will provide good "cleanup" at the very end of a backoff chain, as I have noticed that even my best taggers are missing many, if not most, proper nouns.
