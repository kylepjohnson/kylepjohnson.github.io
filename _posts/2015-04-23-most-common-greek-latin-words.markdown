---
layout: post
title:  "10,000 most frequent words in Greek and Latin canon"
date:   2015-04-23 00:16:00
categories: blog
---

While working on the latest release for the CLTK, which now includes stopword builders, I discovered Python's built-in `Counter().most_common()` method, which makes creating word frequency lists easy ([Greek notebook here](/notebooks/10,000 most common Greek words.html), [Latin here](/notebooks/10,000 most common Latin words.html)). Using some helper methods in the CLTK (namely the PHI and TLG corpus filepath builders and text cleaners), this notebook lists the frequency of words in the TLG corpus.

While a student, the ability to make such lists would have been helpful in optimizing time spent studying vocabulary.

*Greek*: [The 10,000 most common Greek words](/assets/most-common-greek-words.txt), in their inflected forms, in the Classical Greek canon.

*Latin*: [The 10,000 most common Latin words](/assets/most-common-latin-words.txt), in their inflected forms, in the Classical Latin canon.

