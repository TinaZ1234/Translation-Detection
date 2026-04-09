# **Final Project** 
---
## **Research Question**

Can NLP algorithms accurately classify whether a text was originally written in
English or translated into English from a different language?

---
## **Motivation**

Knowing that a text is a translation is important since the author’s original intentions can
become lost in translation. As a reader, if you know that a text is originally written in the
language or if it is the result of a translation can increase your awareness and change
your interpretation of the text.
Different languages carry many subtle differences that can be hard for humans to
perceive, so translations between languages may carry some traces of these language
differences and carry patterns that can be detected by machine learning techniques.

---
## **Data**

https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/ITLGQV
Bag of words data on 10000 english translated texts and 10000 original english texts. A
line in each csv file contains the document ID, the word, and the frequency of that word.
The words in this data appear to already be preprocessed to a certain extent, with the
word frequencies listing things such as “wouldnt” with no apostrophe.

---
## **Planned Methods**

Since we have easier access to bag of words style data from translated and original
texts, Naive Bayes may be a good starting point as it ignores word order. Some
languages express ideas using words or phrases in ways that would rarely occur in
English. However, the fact that Naive Bayes ignores word order can be a big problem.
Different languages have distinct syntactic structures. This could be an important
pattern to note for translations that choose a more literal, one to one approach, leading
to English sentences that feel slightly less natural. As a more extreme example, in
Chinese, the typical sentence order places the time or location before the action. “我昨
天去了学校” would directly translate to “I yesterday went to school”. This ordering of
words is not something you would expect to see in texts originally written in English. If
the Naive Bayes fails, we will find another dataset that includes the full texts rather than
bags of words.

We may choose to not lemmatize or normalize the words further on our first attempt
since the exact version of the words used may potentially be meaningful to discern
between original and translation, but we may try a lemmatized version later and
compare the two.
