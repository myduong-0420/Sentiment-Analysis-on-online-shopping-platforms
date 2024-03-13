# Spam-Classification-on-online-shopping-platforms

This project aims at analyzing lipstick sales on a popular online shopping platform in Vietnam called Shopee using Spam Classification.

---

## 1. Data gathering and preprocessing
### a. Data gathering
Data is gathered from Shopee using ExportComments.com. The chosen shop and product URLs all contain roughly 1000 to 5000 comments, since the extraction tool can only export at most 3030 comments. All of this data is unlabelled.
### Link:
- EXPORT COMMENTS:
  https://exportcomments.com/

### b. Data preprocessing
Data is roughly cleaned and compiled twice using Pandas and Matplotlib. 
- In the first run, irrelevant features like index column, image and video URLs are dropped, row duplicates are removed, columns are renamed and new features like "Product name" and "Duplicated" are added.
- In Vietnamese, syllables separated from one another using a white space, and at least 1 syllable compose a comprehensible word. Thus, in the second run, text data are extracted and segmented using the python-rdrsegmenter library for Vietnamese text segmentation. New features like Char, Segm_count, Word_count, Char/Wcount, Time, Day, Weekday and Rating are added for temporal analysis and spam classification.
  + Char: the number of characters in a sentence (with space)
  + Segm_count: the number of comprehensible words in a sentence
  + Word_count: the number of syllables (tiếng) in a sentence. Sentences with fewer than 4 syllables are highly likely to be spam, because the short length is simply not enough to provide constructive information.
  + Char/Wcount: the number of characters / word count. The character length of Vietnamese syllable typically ranges from 2 to 6, and the maximum length is 7. Sentences with Char/Wcount feature > 5 or < 3.5 are highly likely to be spam. The range (3.5, 5) already accounts for the white space addition.
- Rows with very apparent spam characteristics mentioned (abnormal word counts or Char/Wcount proportion) are removed.

## 2. Data Visualization
Using Pandas and Matplotlib, I was able to extract the temporal patterns of spam reviewers.
