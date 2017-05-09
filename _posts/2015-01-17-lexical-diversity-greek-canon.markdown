---
layout: post
title:  "Lexical diversity in the Greek canon"
date:   2015-01-17 11:25:00
categories: blog
---


This post is just a quick summary of a little calculation I did with the help of the CLTK's improved [text processing for the TLG](http://docs.cltk.org/en/latest/greek.html#converting-tlg-and-phi-texts-with-tlgu). All of my code for this is in my notebook <a href="/notebooks/Lexical diversity in the Greek canon.html">Lexical diversity in the Greek canon</a>, though the most meaningful result I copy below. The following list includes TLG texts with more than 1000 words attributed to an author, which totals to 819 total authors.

Lexical diversity is simply the ratio of total unique words to total words. So a higher lexical diversity means that an author has a richer vocabulary and/or morphology. ([See the NLTK on the subject here](http://www.nltk.org/book/ch01.html).) Please note that this computation is not based on word lemmata, but their inflected form. Once we have an Ancient Greek lemmatizer, this computation should be done again with lemmata, too.

If this sparks any thoughts for you about future development or research, feel free to drop a line via [email](mailto:kyle@kyle-p-johnson.com) or Twitter [@kylepj0hns0n](https://twitter.com/kylepj0hns0n).

```
Author & Genre                                                                        Score
--------------                                                                        -----
Abydenus Hist.                                                                        0.669886
Oracula Chaldaica                                                                     0.657914
Christodorus Epic.                                                                    0.647059
Musaeus Grammaticus Epic.                                                             0.645134
Lycophron Trag.                                                                       0.627297
Hermippus Comic.                                                                      0.625850
Triphiodorus Epic. et Gramm.                                                          0.623535
Glossae In Herodotum                                                                  0.623282
Comica Adespota (FCG)                                                                 0.622345
Colluthus Epic.                                                                       0.621961
Joannes Gramm. et Poeta                                                               0.619838
Bion Bucol.                                                                           0.607708
Philistus Hist.                                                                       0.606364
Solon Nomographus et Poeta                                                            0.604762
Comica Adespota (CAF)                                                                 0.603940
Timotheus Lyr.                                                                        0.601951
Eudemus Rhet.                                                                         0.592703
Anacreon Lyr.                                                                         0.588930
Archelaus Alchem. et Poeta                                                            0.587949
Matron Parodius                                                                       0.584738
Mnaseas Perieg.                                                                       0.578624
Certamen Homeri Et Hesiodi                                                            0.577108
Asclepiades Myth.                                                                     0.572703
[Aristides] Hist.                                                                     0.571545
Heracliti Ephesii Epistulae                                                           0.569485
Moschus Bucol.                                                                        0.567085
Plato Comic.                                                                          0.567001
Alcmaeon Phil.                                                                        0.566572
Quintus Fabius Pictor Hist.                                                           0.560119
Georgius Gramm.                                                                       0.559120
Paulus Silentiarius Poeta                                                             0.557502
Dinon Hist.                                                                           0.553875
Neanthes Hist.                                                                        0.553265
Pherecrates Comic.                                                                    0.550018
Juba II Rex Mauretaniae [Hist.]                                                       0.548547
Demetrius Rhet.                                                                       0.547438
Timocles Comic.                                                                       0.547288
Anaxandrides Comic.                                                                   0.545553
Anonymi Paradoxographi                                                                0.545351
Batrachomyomachia                                                                     0.541427
Eubulus Comic.                                                                        0.541220
Anacreontea                                                                           0.540146
Persaeus Phil.                                                                        0.539451
Severus Soph.                                                                         0.538254
Beros(s)us Astrol. et Hist.                                                           0.534909
Theodorus Heracleensis vel Theodorus Mopsuestenus Scr. Eccl.                          0.534661
Mantissa Proverbiorum                                                                 0.534641
Socratis Epistulae                                                                    0.532746
Archestratus Parodius                                                                 0.532630
Pherecydes Myth. et Phil.                                                             0.531915
Lyrica Adespota (CA)                                                                  0.531268
Hippias Soph.                                                                         0.531001
Demonax Phil.                                                                         0.530153
Androtion Hist.                                                                       0.530144
Diphilus Comic.                                                                       0.529389
Lyrica Adespota (PMG)                                                                 0.528288
Lexicon Artis Grammaticae                                                             0.528053
Vita Et Sententiae Secundi                                                            0.527483
Ister Hist.                                                                           0.527018
Antipater Phil.                                                                       0.524158
Heraclides Lembus Hist.                                                               0.521800
Theodorus Prodromus Poeta et Polyhist.                                                0.521765
Prodicus Soph.                                                                        0.520088
Critolaus Phil.                                                                       0.519841
Lysimachus Hist.                                                                      0.519164
Lexicon De Atticis Nominibus                                                          0.516746
[Theano] Phil.                                                                        0.516714
Acta Justini Et Septem Sodalium                                                       0.512579
Tryphon II Gramm.                                                                     0.511422
Lexicon Patmense                                                                      0.510682
Gaius Suetonius Tranquillus Gramm. et Hist.                                           0.510114
Nicander Epic.                                                                        0.508636
Lesbonax Rhet.                                                                        0.508346
Aristodemus Hist.                                                                     0.505488
Ephraem Scr. Eccl.                                                                    0.505213
Theodosius Diaconus Hist. et Poeta                                                    0.503659
Philippus II Rex Macedonum [Epist.]                                                   0.503306
Alcidamas Rhet.                                                                       0.502991
Heraclitus Phil.                                                                      0.502869
Xanthus Hist.                                                                         0.501745
Thales Phil.                                                                          0.499644
Lexica In Opera Gregorii Nazianzeni                                                   0.499479
Tyrtaeus Eleg.                                                                        0.498843
Anaximenes Phil.                                                                      0.498179
Apollonius Paradox.                                                                   0.497985
Eusebius Phil.                                                                        0.497875
Duris Hist.                                                                           0.496344
Dicaearchus Phil.                                                                     0.495980
Simonides Lyr.                                                                        0.495027
Lexicon Sabbaiticum                                                                   0.495010
Protagoras Soph.                                                                      0.493836
Hegesander Hist.                                                                      0.493387
Epimenides Phil.                                                                      0.491716
Petrus Scr. Eccl. et Theol.                                                           0.491239
Passio Perpetuae Et Felicitatis                                                       0.491059
Marcus Cornelius Fronto Rhet.                                                         0.488924
Epistula Ad Diognetum                                                                 0.488904
Martyrium Polycarpi                                                                   0.488873
Hieronymus Phil.                                                                      0.488818
Phaenias Phil.                                                                        0.488277
Lexicon Rhetoricum Cantabrigiense                                                     0.486516
Praxiphanes Phil.                                                                     0.486408
Herodes Atticus Soph.                                                                 0.486328
Anonymus Photii Phil.                                                                 0.484820
Anaximander Phil.                                                                     0.484607
Chamaeleon Phil.                                                                      0.484108
Oppianus Epic.                                                                        0.484106
Callistratus Soph.                                                                    0.483075
Athenaeus Mech.                                                                       0.482795
Dositheus Magister Gramm.                                                             0.482433
Ptolemaeus Gnost.                                                                     0.481584
Charax Hist.                                                                          0.481563
Epistula Ecclesiarum Apud Lugdunum Et Viennam                                         0.479466
Bolus Med. et Phil.                                                                   0.478755
Rhianus Epic.                                                                         0.476885
Athanasius Soph.                                                                      0.476489
[Hippodamus] Phil.                                                                    0.475924
Dionysius Soph.                                                                       0.475758
Marcellinus Biogr.                                                                    0.475135
Valerius Babrius Scr. Fab.                                                            0.474693
Demetrius Hist. et Phil.                                                              0.474407
Appendix Proverbiorum                                                                 0.473201
Phylarchus Hist.                                                                      0.471016
Cratetis Epistulae                                                                    0.469851
Heraclides Criticus Perieg.                                                           0.469727
Acta Petri                                                                            0.469597
Sententiae Pythagoreorum                                                              0.469514
Minucianus Junior Rhet.                                                               0.469042
[Septem Sapientes] Phil.                                                              0.468294
Martyrium Pionii                                                                      0.467834
Dionysius Geogr.                                                                      0.467391
Herodorus Hist.                                                                       0.465817
Demetrius Gramm.                                                                      0.465124
Theodorus Scutariota Hist.                                                            0.465107
Theodorus Epist.                                                                      0.463896
Anonymus Iamblichi Phil.                                                              0.463228
Hymni Anonymi                                                                         0.463195
Lesbonax Gramm.                                                                       0.463048
Archytas Phil.                                                                        0.463013
Pytheas Perieg.                                                                       0.462355
Ariston Phil.                                                                         0.462030
Acta Barnabae                                                                         0.462009
Demades Orat. et Rhet.                                                                0.461969
Machon Comic.                                                                         0.461666
Ion Phil. et Poeta                                                                    0.461233
Publius Herennius Dexippus Hist.                                                      0.460990
Aristobulus Judaeus Phil.                                                             0.460560
Timaeus Sophista Gramm.                                                               0.459441
Lachares Soph.                                                                        0.458406
Martyrium Ignatii                                                                     0.457851
Polemon Perieg.                                                                       0.457182
Fragmenta Anonyma (PsVTGr)                                                            0.456981
Anatolius Math. et Phil.                                                              0.456944
Timaeus Phil.                                                                         0.456228
Antigonus Paradox.                                                                    0.455771
Sententiae Sexti                                                                      0.455727
Socraticorum Epistulae                                                                0.455653
Melito Apol.                                                                          0.453894
Scholia In Xenophontem                                                                0.453769
Cratinus Comic.                                                                       0.453674
Lexica Segueriana                                                                     0.453131
Vitae Aristotelis                                                                     0.453113
Critias Eleg., Phil. et Trag.                                                         0.452617
Parthenius Myth.                                                                      0.451013
Arsenius Paroemiogr.                                                                  0.450335
Aristides Apol.                                                                       0.449275
Macarius Chrysocephalus Paroemiogr.                                                   0.449239
Moeris Attic.                                                                         0.448745
Callisthenes Hist.                                                                    0.448353
Timotheus Gramm.                                                                      0.446970
Oracula Tiburtina                                                                     0.446883
Liber Jubilaeorum                                                                     0.446613
Cleanthes Phil.                                                                       0.446083
Aeschines Socraticus Phil.                                                            0.445874
Parmenides Poet. Phil.                                                                0.444707
Arethas Philol. et Scr. Eccl.                                                         0.444643
Callixenus Hist.                                                                      0.444626
Synesius Alchem.                                                                      0.442953
Scriptor Incertus De Leone Armenio Hist.                                              0.442421
Marcus Antonius Polemon Soph.                                                         0.441839
Chionis Epistulae                                                                     0.441417
Publius Aelius Phlegon Paradox.                                                       0.440720
Apollonius Phil.                                                                      0.440506
Aratus Astron. et Epic.                                                               0.439875
Didache XII Apostolorum                                                               0.439004
Lexica Syntactica                                                                     0.438647
Sextus Julius Africanus Hist.                                                         0.438214
Apocalypsis Sedrach                                                                   0.437984
Philemon Comic.                                                                       0.437363
[Palaephatus] Myth.                                                                   0.437337
Theognis Eleg.                                                                        0.437044
Philostratus Junior Soph.                                                             0.436118
Maximus Rhet.                                                                         0.435525
Pamprepius Epic.                                                                      0.433395
Philosophus Anonymus Alchem.                                                          0.432458
Zeno Hist.                                                                            0.431845
Ptolemaeus Gramm.                                                                     0.431809
Agathemerus Geogr.                                                                    0.431616
[Pythagoras] Phil.                                                                    0.431415
Bruti Epistulae                                                                       0.431316
Ocellus Phil.                                                                         0.431020
Joannes Anagnostes Hist. et Poeta                                                     0.430515
Lexica Synonymica                                                                     0.430079
Aristaenetus Epist.                                                                   0.429405
Iamblichus Scr. Erot.                                                                 0.429388
Apollonius Soph.                                                                      0.428210
Philosophus Christianus Alchem.                                                       0.428151
Anonymi In Oppiani Opera                                                              0.427903
Diogenianus Phil.                                                                     0.427823
Phoebammon Soph.                                                                      0.427391
Leucippus Phil.                                                                       0.427298
Theocritus Bucol.                                                                     0.427286
Philolaus Phil.                                                                       0.426093
Aphthonius Rhet.                                                                      0.425566
Hesychius Illustrius Hist.                                                            0.424947
Pseudo-Hippocrates Med.                                                               0.424744
Xenophanes Poet. Phil.                                                                0.424696
Damianus Scriptor De Opticis                                                          0.423729
Apollodorus Mech.                                                                     0.422664
Erotianus Gramm. et Med.                                                              0.421859
Pausanias Attic.                                                                      0.421769
Alexis Comic.                                                                         0.421184
Heraclides Ponticus Phil.                                                             0.420969
Tiberius Rhet.                                                                        0.420878
Teles Phil.                                                                           0.420290
[Longinus] Rhet., Pseudo-Longinus                                                     0.420129
Eudocia Augusta Poeta                                                                 0.419816
Satyrus Biogr.                                                                        0.419781
Archigenes Med.                                                                       0.419697
Themistoclis Epistulae                                                                0.418925
Clearchus Phil.                                                                       0.418793
Fragmentum Lexici Graeci                                                              0.418651
Antiphanes Comic.                                                                     0.416391
Scholia In Clementem Alexandrinum                                                     0.415232
Tatianus Apol.                                                                        0.415165
Diogenis Sinopensis Epistulae                                                         0.414543
Hermodorus Phil.                                                                      0.414171
Troilus Soph.                                                                         0.413019
Dionysius Thrax Gramm.                                                                0.412879
Orus Gramm.                                                                           0.412632
Tyrannion Gramm.                                                                      0.412614
Biton Mech.                                                                           0.412088
Megasthenes Hist.                                                                     0.411656
Acusilaus Hist.                                                                       0.410731
Alciphron Rhet. et Soph.                                                              0.410704
Cassius Longinus Phil. et Rhet.                                                       0.410653
Gregorius Paroemiogr.                                                                 0.410373
Cephalion Hist. et Rhet.                                                              0.410304
Bion Phil.                                                                            0.409558
Hermippus Gramm. et Hist.                                                             0.408952
Joannes Cananus Hist.                                                                 0.408878
Hymni Homerici, Homeric Hymns                                                         0.407859
Ignatius Biogr. et Poeta                                                              0.406514
Antisthenes Phil. et Rhet.                                                            0.405688
Alcman Lyr.                                                                           0.405467
Pseudo-Ptolemaeus                                                                     0.403631
Andronicus Rhodius Phil.                                                              0.403624
Zenobius Sophista [Paroemiogr.]                                                       0.403529
Marinus Phil.                                                                         0.402974
Gnomologium Vaticanum                                                                 0.402216
Antonius Hagiographus Scr. Eccl.                                                      0.401879
Archilochus Eleg. et Iamb.                                                            0.401471
Cornelius Alexander Polyhist.                                                         0.401192
Dictys Hist.                                                                          0.400983
Comarius Alchem.                                                                      0.400962
Pherecydes Hist.                                                                      0.400379
Democritus Phil.                                                                      0.400355
Diogenianus Gramm.                                                                    0.399532
Apocalypsis Esdrae                                                                    0.399467
Hermarchus Phil.                                                                      0.399195
Ulpianus Gramm. et Rhet.                                                              0.399089
Apion Gramm.                                                                          0.396807
Josephus Genesius Hist.                                                               0.396747
Olympiodorus Alchem.                                                                  0.396621
Marcellinus I Med.                                                                    0.396584
Prolegomena De Comoedia                                                               0.396387
Manetho Astrol.                                                                       0.395745
Chronographiae Anonymae                                                               0.395105
Lexicon $AI(MWDEI=N                                                                   0.394709
Apocalypsis Baruch                                                                    0.394691
Gorgias Rhet. et Soph.                                                                0.393884
Oenomaus Phil.                                                                        0.393689
Lexicon Vindobonense                                                                  0.393360
Antoninus Liberalis Myth.                                                             0.392903
Priscus Hist. et Rhet.                                                                0.392682
Joannes Pediasimus Philol. et Rhet.                                                   0.392357
Georgius Pisides Poeta                                                                0.392147
Numenius Phil.                                                                        0.391847
Anonymi Geographiae Expositio Compendiaria                                            0.390150
Barnabae Epistula                                                                     0.390149
Aelius Dionysius Attic.                                                               0.389886
Diodorus Scr. Eccl.                                                                   0.389684
Joannes Protospatharius Gramm.                                                        0.388945
Apocalypsis Joannis                                                                   0.388873
Pseudo-Polemon                                                                        0.388581
Scholia In Isocratem                                                                  0.388518
Cyrus Rhet.                                                                           0.386999
Philogelos                                                                            0.386780
Antiphon Soph.                                                                        0.385943
Moses Alchem.                                                                         0.385789
Menandri Et Philistionis Sententiae                                                   0.385719
Aeneas Tact.                                                                          0.383479
Memnon Hist.                                                                          0.381635
Scylitzes Continuatus                                                                 0.380909
Apollodorus Gramm.                                                                    0.380831
Lucius Annaeus Cornutus Phil.                                                         0.380105
Joannes Tzetzes Gramm. et Poeta                                                       0.379989
Scholia In Dionysium Periegetam                                                       0.379857
Constantinus Manasses Hist. et Poeta                                                  0.379686
Orphica                                                                               0.378739
Scholia In Oppianum                                                                   0.378337
Paraleipomena Jeremiou                                                                0.377719
Alexander Rhet. et Soph.                                                              0.377646
Bacchylides Lyr.                                                                      0.377066
Dioscorus Poeta                                                                       0.375933
Joannes Theol.                                                                        0.375524
[Ammonius] Gramm.                                                                     0.375400
Scholia In Callimachum                                                                0.374620
[Cebes] Phil.                                                                         0.374406
Scylax Perieg.                                                                        0.374364
Dionysius Scytobrachion Gramm.                                                        0.374261
Anonymi Geographia In Sphaera Intelligenda                                            0.374175
Trophonius Rhet. et Soph.                                                             0.373333
Dionysius Perieg.                                                                     0.373201
Eratosthenes et Eratosthenica Philol.                                                 0.372798
Onasander Tact.                                                                       0.372756
Anthemius Math. et Mech.                                                              0.372208
Acta Phileae                                                                          0.372180
Atticus Phil.                                                                         0.371971
Apollonius Rhodius Epic.                                                              0.371905
Longus Scr. Erot.                                                                     0.371595
Philochorus Hist.                                                                     0.371485
Acta Pauli                                                                            0.371105
Pseudo-Dioscorides Med.                                                               0.370982
Eutecnius Soph.                                                                       0.370789
Empedocles Poet. Phil.                                                                0.370735
Philumenus Med.                                                                       0.370574
Pythagoristae (D-K) Phil.                                                             0.370539
Attalus Astron. et Math.                                                              0.369872
Evangelium Bartholomaei                                                               0.369395
Anonymi In Aphthonium Rhet.                                                           0.369145
Leontius Mech.                                                                        0.369128
Theopompus Hist.                                                                      0.368699
Periplus Maris Erythraei                                                              0.368109
Ninus                                                                                 0.367444
Anthologiae Graecae Appendix                                                          0.366212
Manetho Hist.                                                                         0.366192
Epicharmus Comic. et Pseudepicharmea                                                  0.366191
Severus Iatrosophista Med.                                                            0.365924
Patria Constantinopoleos                                                              0.365870
Cassius Iatrosophista Med.                                                            0.365730
Zeno Phil.                                                                            0.364116
Tryphon I Gramm.                                                                      0.363520
Callimachus Philol.                                                                   0.362854
Alexander Scr. Eccl.                                                                  0.361881
Symeon Metaphrastes Biogr. et Hist.                                                   0.361092
Testamentum Jobi                                                                      0.360715
Philostratus Major Soph.                                                              0.359560
Dialexeis  ($*DISSOI\ LO/GOI)                                                         0.359301
Maximus Astrol.                                                                       0.359054
Aeneas Phil. et Rhet.                                                                 0.358839
Periplus Ponti Euxini                                                                 0.358268
Pseudo-Apollodorus Myth.                                                              0.358031
Lycurgus Orat.                                                                        0.357885
Acta Joannis                                                                          0.357823
Pseudo-Auctores Hellenistae (PsVTGr)                                                  0.357603
Marcus Diaconus Scr. Eccl.                                                            0.357279
Joel Chronogr.                                                                        0.357143
Historia Monachorum In Aegypto                                                        0.356863
Ephorus Hist.                                                                         0.356442
Comica Adespota (Suppl. Com.)                                                         0.356426
Favorinus Phil. et Rhet.                                                              0.355432
Oracula Sibyllina                                                                     0.355254
Maximus Theol.                                                                        0.355194
Adamantius Judaeus Med.                                                               0.355177
Anaxagoras Phil.                                                                      0.354637
Agatharchides Geogr.                                                                  0.354351
Eudoxus Astron.                                                                       0.354127
Melissus Phil.                                                                        0.353677
[Demetrius] Rhet.                                                                     0.353026
Vita Adam Et Evae                                                                     0.352671
Protevangelium Jacobi                                                                 0.352308
Acta Xanthippae Et Polyxenae                                                          0.351866
Scholia In Lucianum                                                                   0.351810
Aristocles Phil.                                                                      0.351564
Hierophilus Phil. et Soph.                                                            0.350815
Anonymus De Scientia Politica Hist.                                                   0.350333
Straton Phil.                                                                         0.350242
Physiologus                                                                           0.350140
Philostorgius Scr. Eccl.                                                              0.349393
Eunapius Hist. et Soph.                                                               0.348685
Vitae Arati Et Varia De Arato                                                         0.348652
Anonymi Exegesis In Hesiodi Theogoniam                                                0.347007
Sallustius Phil.                                                                      0.347002
Aristeae Epistula                                                                     0.345921
Choerilus Epic.                                                                       0.344991
Phalaridis Epistulae                                                                  0.344988
Aristophanes Gramm.                                                                   0.344654
Michael Apostolius Paroemiogr.                                                        0.344441
Anonymus Seguerianus Rhet.                                                            0.344165
Gaius Musonius Rufus Phil.                                                            0.343675
Timaeus Hist.                                                                         0.343652
Vitae Homeri                                                                          0.343640
Etymologicum Parvum                                                                   0.342745
Alexander Theol.                                                                      0.342539
Albinus Phil.                                                                         0.341526
Herodas Mimogr.                                                                       0.341352
Asterius Scr. Eccl.                                                                   0.341198
Callinicus Biogr.                                                                     0.340907
Joannes Galenus Gramm.                                                                0.340427
Joannes Cameniates Hist.                                                              0.340354
Anonymi In Aristotelis Librum Primum Analyticorum Posteriorum Commentarium            0.340322
Teucer Astrol.                                                                        0.340316
Eustathius Scr. Eccl. et Theol.                                                       0.340218
Pseudo-Nonnus                                                                         0.339651
Pseudo-Lucianus Soph.                                                                 0.339421
Hephaestion Gramm.                                                                    0.339315
Hesychius Lexicogr.                                                                   0.336806
Hipponax Iamb.                                                                        0.336679
Leo Diaconus Hist.                                                                    0.336411
Theophilus Apol.                                                                      0.335412
Didymus Gramm.                                                                        0.335100
Ae+tius Doxogr.                                                                       0.334523
Aristoxenus Mus.                                                                      0.334241
Xenophon Scr. Erot.                                                                   0.333931
Anonymi De Astrologia Dialogus Astrol.                                                0.333137
Thessalus Astrol. et Med.                                                             0.332026
Celsus Phil.                                                                          0.331178
Thomas Magister Philol.                                                               0.330197
Pseudo-Symeon Hist.                                                                   0.330070
Eutropius Hist.                                                                       0.330038
Ctesias Hist. et Med.                                                                 0.329919
Scholia In Apollonium Rhodium                                                         0.329334
Joannes Med.                                                                          0.328372
Philo Mech.                                                                           0.326527
Erasistratus Med.                                                                     0.325872
Andocides Orat.                                                                       0.325746
Anaximenes Hist. et Rhet.                                                             0.325260
Chariton Scr. Erot.                                                                   0.324947
Anthologia Graeca, AG                                                                 0.324125
Pindarus Lyr.                                                                         0.323948
Anonymi Historici (FGrH)                                                              0.323818
Gregorius Thaumaturgus Scr. Eccl.                                                     0.323449
Gennadius I Scr. Eccl.                                                                0.323417
Vitae Prophetarum                                                                     0.322951
Heraclides Gramm.                                                                     0.321815
Hesychius Scr. Eccl.                                                                  0.321408
Pseudo-Archytas Phil.                                                                 0.320584
Nicephorus Bryennius Hist.                                                            0.319893
Michael Attaliates Hist.                                                              0.319760
Hecataeus Hist.                                                                       0.319506
Rufus Med.                                                                            0.318537
Stephanus Alchem.                                                                     0.318141
Menander Protector Hist.                                                              0.317239
Leo Phil.                                                                             0.317176
Etymologicum Symeonis                                                                 0.316821
Pseudo-Zonaras Lexicogr.                                                              0.316726
Georgius Monachus Continuatus                                                         0.316106
Arcadius Gramm.                                                                       0.315914
Leo Magentinus Phil.                                                                  0.315689
Hyperides Orat.                                                                       0.314956
(H)eren(n)ius Philo Gramm. et Hist.                                                   0.314762
Paraphrases In Dionysium Periegetam                                                   0.314437
Nicolaus Hist.                                                                        0.313808
Orion Gramm.                                                                          0.311966
Stephanus Gramm.                                                                      0.311806
Aesopus Scr. Fab. et Aesopica                                                         0.311771
Hellanicus Hist.                                                                      0.311384
Pseudo-Scymnus Geogr.                                                                 0.310694
Scholia In Theocritum                                                                 0.310435
Scholia In Nicandrum                                                                  0.310372
Horapollo Gramm.                                                                      0.309900
Evagrius Scholasticus Scr. Eccl.                                                      0.309643
Cleonides Mus.                                                                        0.309499
Anonymus De Philosophia Platonica Phil.                                               0.309426
Apollonius Med.                                                                       0.309333
Scholia In Aeschinem                                                                  0.309236
Liber Enoch                                                                           0.308152
Marcus Aurelius Antoninus Imperator Phil.                                             0.306890
Joannes Antiochenus Hist.                                                             0.306670
Dinarchus Orat.                                                                       0.306653
Valerius Apsines Rhet.                                                                0.306350
Nicephorus II Phocas Imperator Tact.                                                  0.305771
Himerius Soph.                                                                        0.303568
Palladius Scr. Eccl.                                                                  0.303222
Ephraem Hist. et Poeta                                                                0.302782
Josephus Et Aseneth                                                                   0.302776
Theodorus Scr. Eccl.                                                                  0.302580
Aelianus Tact.                                                                        0.302003
Aristides Quintilianus Mus.                                                           0.301496
Phrynichus Attic.                                                                     0.300688
Aelius Theon Rhet.                                                                    0.300478
Acta Philippi                                                                         0.299767
Harpocration Gramm.                                                                   0.299705
Asclepiodotus Tact.                                                                   0.299528
Heliodorus Scr. Erot.                                                                 0.298155
Leontius Scr. Eccl.                                                                   0.297888
Ignatius Scr. Eccl.                                                                   0.296949
Theophylactus Simocatta Epist. et Hist.                                               0.296403
Menander Rhet.                                                                        0.295885
Hierocles Phil.                                                                       0.295883
Herodianus Hist.                                                                      0.295391
Strattis Comic.                                                                       0.294899
Theophilus Protospatharius et Stephanus Atheniensis Med.                              0.294676
Antiphon Orat.                                                                        0.294535
Ammonius Scr. Eccl.                                                                   0.294437
Epica Adespota (GDRK)                                                                 0.294108
Speusippus Phil.                                                                      0.293920
Anonymi Medici Med.                                                                   0.293826
Dorotheus Astrol.                                                                     0.293814
Achilles Tatius Scr. Erot.                                                            0.293129
Testamentum Abrahae                                                                   0.292665
Euphorion Epic.                                                                       0.292538
Testamenta XII Patriarcharum                                                          0.291464
Julius Pollux Gramm.                                                                  0.291112
Sappho Lyr.                                                                           0.290261
Vitae Aesopi                                                                          0.289317
Anonymus Dialogus Cum Judaeis                                                         0.289246
Apollinaris Theol.                                                                    0.288877
Cyranides                                                                             0.288768
Basilius Med. et Scr. Eccl.                                                           0.288382
Joannes Gramm. et Theol.                                                              0.287087
Anonyma De Musica Scripta Bellermanniana                                              0.286895
Julianus Scr. Eccl.                                                                   0.286085
Joannes Cinnamus Gramm. et Hist.                                                      0.285961
Xenocrates Phil.                                                                      0.285433
Agathias Scholasticus Epigr. et Hist.                                                 0.284099
Sophronius Gramm.                                                                     0.283898
Polyaenus Rhet.                                                                       0.283756
Fragmenta Alchemica                                                                   0.283087
Scholia in Maximum Confessorem                                                        0.282372
Antimachus Eleg. et Epic.                                                             0.281991
Testamentum Salomonis                                                                 0.281798
Zosimus Alchem.                                                                       0.281560
Eudemus Phil.                                                                         0.281166
Georgius Acropolites Hist.                                                            0.280140
Quintus Epic.                                                                         0.279892
Soranus Med.                                                                          0.279885
Georgius Sphrantzes Hist.                                                             0.279875
Theophanes Continuatus                                                                0.279388
Dionysius Epic.                                                                       0.279058
Nicetas Choniates Hist., Scr. Eccl. et Rhet.                                          0.278776
Synesius Phil.                                                                        0.278400
Corpus Hermeticum                                                                     0.278058
Achilles Tatius Astron.                                                               0.276915
Rhetorica Anonyma                                                                     0.276780
Irenaeus Theol.                                                                       0.276269
Magica                                                                                0.275227
Acta Thomae                                                                           0.275201
Athenagoras Apol.                                                                     0.274809
Hesiodus Epic.                                                                        0.274335
Periplus Maris Magni                                                                  0.274173
Maximus Soph.                                                                         0.273407
Amphilochius Scr. Eccl.                                                               0.273167
Aeschines Orat.                                                                       0.272544
Theodorus Theol.                                                                      0.271725
Pseudo-Codinus Hist.                                                                  0.271185
Symeon Logothetes Hist.                                                               0.271116
Cercidas Iamb.                                                                        0.269852
Claudius Aelianus Soph.                                                               0.269843
Posidonius Phil.                                                                      0.269649
Paulus Astrol.                                                                        0.269374
Diogenes Phil.                                                                        0.268921
Scholia In Lycophronem                                                                0.268854
Nicolaus Rhet. et Soph.                                                               0.268696
Stephanus Med.                                                                        0.268184
Pseudo-Plutarchus                                                                     0.268155
Satyrus Hist.                                                                         0.268031
Zosimus Hist.                                                                         0.268023
Geoponica                                                                             0.267890
Marcianus Geogr.                                                                      0.266769
Choricius Rhet. et Soph.                                                              0.265031
Anonymus Discipulus Isidori Milesii Mech.                                             0.264583
Ducas Hist.                                                                           0.264567
Anonymi Grammatici Gramm.                                                             0.263499
Eupolis Comic.                                                                        0.262526
Adespota Papyracea (SH)                                                               0.262214
Scholia In Aristotelem                                                                0.261801
Cyrillus Biogr.                                                                       0.260879
Nicomachus Math.                                                                      0.260543
Epica Adespota (CA)                                                                   0.260285
Aretaeus Med.                                                                         0.258561
Epimerismi                                                                            0.258199
Artemidorus Onir.                                                                     0.257423
Basilius Scr. Eccl.                                                                   0.257419
Joannes Laurentius Lydus Hist.                                                        0.257089
Asterius Sophista Scr. Eccl.                                                          0.256955
Melampus Scriptor De Divinatione                                                      0.255901
Palladius Med.                                                                        0.255682
Etymologicum Genuinum                                                                 0.254516
Constitutiones Apostolorum                                                            0.254503
Sophocles Trag.                                                                       0.253039
Michael Glycas Astrol. et Hist.                                                       0.252704
Doctrina Patrum                                                                       0.251946
Flavius Claudius Julianus Imperator Phil., Julian the Apostate                        0.249898
Priscianus Phil.                                                                      0.249207
Cleomedes Astron.                                                                     0.248922
Polystratus Phil.                                                                     0.248588
Scholia In Hesiodum                                                                   0.247514
Anonymi Commentarius In Platonis Theaetetum                                           0.246246
Oecumenius Phil. et Rhet.                                                             0.246139
Joannes Doxapatres Rhet.                                                              0.246008
Joannes Camaterus Astrol. et Astron.                                                  0.245827
Meletius Med.                                                                         0.245693
Aristonicus Gramm.                                                                    0.245619
Scholia In Euripidem                                                                  0.245417
Philoxenus Gramm.                                                                     0.244875
Adamantius Theol.                                                                     0.244787
Nicephorus I Scr. Eccl., Hist. et Theol.                                              0.244723
Florilegium Cyrillianum                                                               0.244382
Arius Didymus Doxogr.                                                                 0.244049
Salaminius Hermias Sozomenus Scr. Eccl.                                               0.243816
Photius Lexicogr., Scr. Eccl. et Theol.                                               0.243672
Severianus Scr. Eccl.                                                                 0.243441
Nicolaus I Mysticus Theol. et Epist.                                                  0.241965
Suda, Suidas                                                                          0.241360
Manuel Philes Poeta et Scr. Rerum Nat.                                                0.241250
Isaeus Orat.                                                                          0.241102
Flavius Philostratus Soph.                                                            0.240844
Diogenes Laertius Biogr.                                                              0.239964
Joannes Scylitzes Hist.                                                               0.239922
Nemesius Theol.                                                                       0.239021
Etymologicum Gudianum                                                                 0.238308
Socrates Scholasticus Hist.                                                           0.237658
Olympiodorus Diaconus Scr. Eccl.                                                      0.237100
Pseudo-Dionysius Areopagita Scr. Eccl. et Theol.                                      0.237088
Pseudo-Sphrantzes Hist.                                                               0.237026
Nonnus Epic.                                                                          0.236992
Anna Comnena Hist.                                                                    0.236952
Ibycus Lyr.                                                                           0.236834
Romanus Melodus Hymnographus                                                          0.236709
Theophilus Protospatharius Med.                                                       0.236479
Marcellus Theol.                                                                      0.236419
Scholia In Aratum                                                                     0.235907
Aristophanes Comic.                                                                   0.235658
Alcaeus Lyr.                                                                          0.234926
Lysias Orat.                                                                          0.234578
Pseudo-Mauricius Tact.                                                                0.234359
Scholia In Thucydidem                                                                 0.233895
Geminus Astron.                                                                       0.233274
Cyrillus Scr. Eccl.                                                                   0.233257
Scholia In Platonem                                                                   0.232817
Epictetus Phil.                                                                       0.232642
Georgius Syncellus Chronogr.                                                          0.232293
Tragica Adespota                                                                      0.231480
Flavius Arrianus Hist. et Phil.                                                       0.230979
Aeschylus Trag.                                                                       0.229395
Hermas Scr. Eccl., Pastor Hermae                                                      0.229356
Lyrica Adespota (SLG)                                                                 0.229068
Dexippus Phil.                                                                        0.228844
Scholia In Sophoclem                                                                  0.228697
Acta Alexandrinorum                                                                   0.227098
Hermias Phil.                                                                         0.226885
Chrysippus Phil.                                                                      0.224649
Etymologicum Magnum                                                                   0.223501
Erotica Adespota                                                                      0.221577
Pseudo-Galenus Med.                                                                   0.221170
Theophanes Confessor Chronogr.                                                        0.220965
Hippolytus Scr. Eccl.                                                                 0.220895
Theognostus Gramm.                                                                    0.220577
Anonymi In Aristotelis Categorias Phil.                                               0.219753
Anonymi In Aristotelis Artem Rhetoricam Rhet.                                         0.219733
Cosmas Indicopleustes Geogr.                                                          0.219390
Hippiatrica                                                                           0.218128
Hellenica                                                                             0.217788
Michael Critobulus Hist.                                                              0.217591
Lollianus Scr. Erot.                                                                  0.217172
Corinna Lyr.                                                                          0.215352
Anonymi In Aristotelis Librum Alterum Analyticorum Posteriorum Commentarium           0.214002
Comica Adespota (CGFPR)                                                               0.213854
Joannes Malalas Chronogr.                                                             0.213255
Athenaeus Soph.                                                                       0.212154
Scholia In Diophantum                                                                 0.211835
Syrianus Phil.                                                                        0.210452
Theodorus Studites Scr. Eccl. et Theol.                                               0.209258
Lucianus Soph.                                                                        0.208945
Joannes Actuarius Med.                                                                0.208932
Euripides Trag.                                                                       0.207038
Gregorius Nazianzenus Theol.                                                          0.206543
Clemens Alexandrinus Theol.                                                           0.206109
Chronicon Paschale                                                                    0.205748
Theophilus Protospatharius, Damascius et Stephanus Atheniensis Med.                   0.205508
Anonymi In Aristotelis Librum De Interpretatione Phil.                                0.205427
Georgius Pachymeres Hist.                                                             0.204036
Herodotus Hist.                                                                       0.203609
Dio Chrysostomus Soph.                                                                0.202591
Justinus Martyr Apol.                                                                 0.202459
Theon Phil.                                                                           0.201892
Scholia In Pindarum                                                                   0.201335
Georgius Cedrenus Chronogr.                                                           0.198756
Maximus Confessor Theol.                                                              0.198394
Joannes Rhet.                                                                         0.197894
Scholia In Homerum                                                                    0.197853
Procopius Rhet. et Scr. Eccl.                                                         0.197329
Stesichorus Lyr.                                                                      0.197110
Hermogenes Rhet.                                                                      0.196807
Stephanus Med. et Phil.                                                               0.196359
Philodemus Phil.                                                                      0.195780
Georgius Monachus Chronogr.                                                           0.194202
Scholia In Aristophanem                                                               0.194102
Epicurus Phil.                                                                        0.193533
Strabo Geogr.                                                                         0.193387
Dioscorides Pedanius Med.                                                             0.192197
Anonymus Londinensis Med.                                                             0.191474
Joannes Zonaras Gramm. et Hist.                                                       0.190998
Pausanias Perieg.                                                                     0.189998
Evagrius Scr. Eccl.                                                                   0.189973
Paulus Med.                                                                           0.187405
Appianus Hist.                                                                        0.186856
Novum Testamentum, New Testament                                                      0.186761
Anonymi In Aristotelis Sophisticos Elenchos Phil.                                     0.186067
Joannes Stobaeus Anthologus                                                           0.185642
Laonicus Chalcocondyles Hist.                                                         0.184319
Sophonias Phil.                                                                       0.183943
Hypsicles Astron. et Math.                                                            0.183765
Clemens Romanus Theol. et Clementina                                                  0.183682
Scholia In Demosthenem                                                                0.183639
Thucydides Hist.                                                                      0.181335
Anonymus Manichaeus Biogr.                                                            0.180590
Theodosius Gramm.                                                                     0.180335
Apollonius Dyscolus Gramm.                                                            0.179285
Iamblichus Phil.                                                                      0.178956
Stephanus Phil.                                                                       0.178553
Philo Judaeus Phil.                                                                   0.178513
Theophrastus Phil.                                                                    0.178190
Michael Psellus Polyhist.                                                             0.177303
Pseudo-Justinus Martyr                                                                0.175328
Vettius Valens Astrol.                                                                0.175290
Nicephorus Gregoras Hist.                                                             0.175068
Isocrates Orat.                                                                       0.174664
Porphyrius Phil.                                                                      0.174077
Menander Comic.                                                                       0.173153
Scholia In Aeschylum                                                                  0.173104
Homerus Epic., Homer                                                                  0.171125
Flavius Josephus Hist.                                                                0.170452
Aspasius Phil.                                                                        0.170014
Ephraem Syrus Theol.                                                                  0.169239
Alexander Med.                                                                        0.168708
Anonymus Epicureus Phil.                                                              0.168171
Aelius Herodianus et Pseudo-Herodianus Gramm. et Rhet.                                0.167883
Scholia In Aelium Aristidem                                                           0.167480
Commentaria In Dionysii Thracis Artem Grammaticam                                     0.167415
Apophthegmata                                                                         0.163883
Dionysius Halicarnassensis Hist. et Rhet.                                             0.163435
Procopius Hist.                                                                       0.161663
Polybius Hist.                                                                        0.160925
Xenophon Hist.                                                                        0.159942
Plutarchus Biogr. et Phil.                                                            0.158461
Flavius Justinianus Imperator Theol.                                                  0.156614
Epiphanius Scr. Eccl.                                                                 0.156212
Joannes Damascenus Scr. Eccl. et Theol., John of Damascus                             0.154918
Ae+tius Med.                                                                          0.154320
Pseudo-Macarius Scr. Eccl.                                                            0.152753
Georgius Choeroboscus Gramm.                                                          0.151996
Apomasar Astrol.                                                                      0.151006
Olympiodorus Phil.                                                                    0.149872
Sextus Empiricus Phil.                                                                0.148276
Constantinus VII Porphyrogenitus Imperator Hist.                                      0.148058
Diodorus Siculus Hist.                                                                0.147006
Aelius Aristides Rhet.                                                                0.145784
[Astrampsychus Magus] Onir.                                                           0.145544
Sopater Rhet.                                                                         0.145469
Joannes VI Cantacuzenus                                                               0.145243
Historia Alexandri Magni                                                              0.142985
Claudius Ptolemaeus Math.                                                             0.142923
Hippocrates Med. et Corpus Hippocraticum                                              0.141236
Libanius Rhet. et Soph.                                                               0.139806
Demosthenes Orat.                                                                     0.139573
Anonymi In Hermogenem Rhet.                                                           0.139361
Hephaestion Astrol.                                                                   0.138991
Aristarchus Astron.                                                                   0.136486
Oribasius Med.                                                                        0.135322
Eustratius Phil.                                                                      0.134103
Elias Phil.                                                                           0.133826
David Phil.                                                                           0.132742
Eustathius Philol. et Scr. Eccl.                                                      0.132091
Didymus Caecus Scr. Eccl., Didymus the Blind                                          0.131580
Anonymi In Aristotelis Ethica Nicomachea Phil.                                        0.131489
Basilius Theol.                                                                       0.131071
Gregorius Nyssenus Theol.                                                             0.130243
Damascius Phil.                                                                       0.129953
Cassius Dio Hist., Dio Cassius                                                        0.129384
Athanasius Theol.                                                                     0.127427
Hipparchus Astron. et Geogr.                                                          0.126379
Syriani, Sopatri Et Marcellini Scholia Ad Hermogenis Status                           0.125763
Plato Phil.                                                                           0.123329
Septuaginta                                                                           0.121475
Concilia Oecumenica (ACO)                                                             0.118851
Origenes Theol.                                                                       0.116731
Michael Phil.                                                                         0.116180
Eutocius Math.                                                                        0.116171
Plotinus Phil.                                                                        0.112597
Eusebius Scr. Eccl. et Theol.                                                         0.112009
Aristoteles Phil. et Corpus Aristotelicum, Aristotle                                  0.109306
Barlaam Math., Theol. et Epist.                                                       0.107771
Catenae (Novum Testamentum)                                                           0.104460
Diophantus Math.                                                                      0.104070
Asclepius Phil.                                                                       0.103895
Ammonius Phil.                                                                        0.102155
Theodoretus Scr. Eccl. et Theol.                                                      0.102138
Carneiscus Phil.                                                                      0.097053
Galenus Med.                                                                          0.092537
Autolycus Astron.                                                                     0.090733
Archimedes Geom.                                                                      0.090540
Themistius Phil. et Rhet.                                                             0.090107
Proclus Phil.                                                                         0.085679
Cyrillus Theol.                                                                       0.083460
Theon Math.                                                                           0.082577
Scholia In Euclidem                                                                   0.080507
Heron Mech.                                                                           0.079829
Pappus Math.                                                                          0.077954
Serenus Geom.                                                                         0.074851
Apollonius Geom.                                                                      0.073367
Theodosius Astron. et Math.                                                           0.070494
Alexander Phil.                                                                       0.070338
Simplicius Phil.                                                                      0.068388
Joannes Chrysostomus Scr. Eccl., John Chrysostom                                      0.065196
Joannes Philoponus Phil.                                                              0.064113
Euclides Geom.                                                                        0.046822
```
