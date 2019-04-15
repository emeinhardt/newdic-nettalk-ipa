# newdic-nettalk-ipa
Mike Hammond's newdic / Sejnowski &amp; Rosenberg's NETtalk dictionary, but with Unicode IPA symbols.

## Context

Prof. Mike Hammond has a transcribed and annotated dictionary of American English located at 
 - http://dingo.sbs.arizona.edu/~hammond/lsasummer11/newdic

There's no documentation I'm aware of as to where any of this information came from. It was used to help create the inventory of American English diphones for Warner et al. 2014 ("Tracking the perception of the sounds of English").

If you google some of the transcriptions, it appears the transcriptions are the same as those in the 'NETtalk corpus' of Sejnowski & Rosenberg 1987 ("Parallel networks that learn to pronounce English text"). The dataset can be found at UCI's Machine Learning Repository here
 - https://archive.ics.uci.edu/ml/datasets/Connectionist+Bench+(Nettalk+Corpus)
 
Both `newdic.txt` and `nettalk.data` are included in this repository. The two files are not identical and contain slightly different annotations about each entry; newdic appears to contain about 500 fewer entries.

## About the transcriptions

The text of Sejnowski & Rosenberg indicates that the transcriptions came from an unspecified version of *Meriam Webster's Pocket Dictionary*. (In other words, we have no systematic information or documentation about what the inventory is or what the assumptions of the transcribers were.)

Each line of both dictionaries associates an orthographic wordform with a transcription, information about stress and syllabic structure, and other information. In the case of `nettalk.data`, this is an integer indicating whether the word is foreign or irregular. In the case of `newdic.txt`, this is a column explicitly indicating which syllable (counting from the left) has primary stress, what might be frequency count information (from an unknown dataset), and a list of part-of-speech tags that the orthographic wordform can have (based on an unknown dataset or annotation procedure).

There are about 20k entries in each file and each associates an orthographic wordform with exactly one transcription.

## This repository

The Jupyter notebook in this repository converts the transcriptions in `newdic.txt` to Unicode IPA symbols and documents my choices / my process of identifying correspondences.

The notebook uses Python 3. (Note that Python /3/ makes Unicode much more straightforward and painless to deal with than Python 2.) There are no other salient dependencies.
