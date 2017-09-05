---
layout: post
title:  "Tf-idf pairwise similarity in the Greek canon"
date:   2015-04-02 7:45:00
categories: blog
---

I may write more about this later, but I have been sitting on this Greek tf-idf pairwise similarity comparison, run on all authors of the TLG against one another, for too long time already. Here is a compressed file for [all possible tf-idf pairwise similarity comparisons (3,157,729 total) for the Ancient Greek canon](/assets/tlg_tfidf_pairwise_sims_final.tar.gz) (40 MB compressed, 191 MB uncompressed).

For an glimpse at what it contains, consider here some comparisons of Thucydides to other "canonical" authors …

poets:

```
 'Thucydides Hist. v. Hesiodus Epic.': '0.60464602',

 'Thucydides Hist. v. Homerus Epic., Homer': '0.55499628',
 
 'Thucydides Hist. v. Pindarus Lyr.': '0.52949028',
```

other historians:

```
 'Thucydides Hist. v. Herodotus Hist.': '0.81607810',
 
 'Thucydides Hist. v. Xenophon Hist.': '0.88050189',
 
 'Thucydides Hist. v. Polybius Hist.': '0.82481702',
```

other prose authors:

```
'Thucydides Hist. v. Aristoteles Phil. et Corpus Aristotelicum, Aristotle': '0.82249181',
 
 'Thucydides Hist. v. Plato Phil.': '0.82874397',
 
 'Thucydides Hist. v. Plutarchus Biogr. et Phil.': '0.89397022',
```

tragedians:

```
 'Thucydides Hist. v. Aeschylus Trag.': '0.67016340',
 
 'Thucydides Hist. v. Euripides Trag.': '0.59366905',
 
 'Thucydides Hist. v. Sophocles Trag.': '0.55533646',
```

What all this means – well, I'll leave that for another day. As always, here's [the IPython notebook I used for the task](/notebooks/Tf-idf pairwise similarity, Greek.html).