# Sentiment-Analysis-on-online-shopping-platforms

This project aims at analyzing lipstick sales on a popular online shopping platform in Vietnam called Shopee using Spam Classification and Sentiment Analysis with #(will work on this)VinaLLaMA# - a Vietnamese Large Language Model.

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
- In the second run, text data are extracted and segmented using the python-rdrsegmenter library for Vietnamese text segmentation. New features like Char, Segm_count, Word_count, Char/Wcount, Time, Day, Weekday and Rating are added for temporal analysis and spam classification.
