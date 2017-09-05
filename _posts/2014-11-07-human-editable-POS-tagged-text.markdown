---
layout: post
title:  "A human–editable POS–tagged text"
date:   2014-11-07 19:48:00
categories: blog
---

Since I have begun talking about POS tagging with the CLTK, my educator contacts have been asking about ways they and their students can contribute. I am happy to share [greek\_pos\_edit\_xenophon\_anabasis](https://github.com/cltk/greek_pos_edit_xenophon_anabasis) (not a very compelling name, I know), which contains all of Xenophon's *Anabasis* tagged with the CLTK's latest version of the TnT tagger (on which, [read more here](/blog/2014/10/25/tnt-pos-taggers-with-cltk.html)).

I have taken pains to make these files easy to read and edit. With GitHub, anyone can edit in–browser, which I think will lower the bar to entry and allow any student of Greek to contribute.

Below is an example of a corrected sentence. See here in–progress editing of [*Anabasis* 1](https://github.com/cltk/greek_pos_edit_xenophon_anabasis/blob/master/pos_editable_xenophon_anabasis_1.md).

>## Sentence 1
### Plaintext
Δαρείου καὶ Παρυσάτιδος γίγνονται παῖδες δύο, πρεσβύτερος μὲν Ἀρταξέρξης, νεώτερος δὲ Κῦρος· ἐπεὶ δὲ ἠσθένει Δαρεῖος καὶ ὑπώπτευε τελευτὴν τοῦ βίου, ἐβούλετο τὼ παῖδε ἀμφοτέρω παρεῖναι.

>### Tagged
```
('Δαρείου', 'N-S---MG-')
('καὶ', 'C--------')
('Παρυσάτιδος', 'N-S---FG-')
('γίγνονται', 'V3PPIE---')
('παῖδες', 'N-P---MN-')
('δύο', 'M--------')
(',', 'U--------')
('πρεσβύτερος', 'A-S---MNC')
('μὲν', 'G--------')
('Ἀρταξέρξης', 'N-S---MN-')
(',', 'U--------')
('νεώτερος', 'N-S---MN-')
('δὲ', 'G--------')
('Κῦρος', 'N-S---MN-')
('·', 'U--------')
('ἐπεὶ', 'C--------')
('δὲ', 'G--------')
('ἠσθένει', 'V-3SIIA--')
('Δαρεῖος', 'N-S---MN-')
('καὶ', 'C--------')
('ὑπώπτευε', 'V-3SIIA--')
('τελευτὴν', 'N-S---FA-')
('τοῦ', 'L-S---MG-')
('βίου', 'N-S---MG-')
(',', 'U--------')
('ἐβούλετο', 'V3SIIE---')
('τὼ', 'L-D---MA-')
('παῖδε', 'N-D---MA-')
('ἀμφοτέρω', 'A-D---MA-')
('παρεῖναι', 'V--PNA---')
('.', 'U--------')


>### Unknown words
['Παρυσάτιδος', 'Ἀρταξέρξης', 'ἠσθένει', 'ὑπώπτευε']
### Corrected by
['kylepjohnson']
