# Sentiment-Analysis-on-online-shopping-platforms

This project aims at analyzing lipstick sales on a popular online shopping platform in Vietnam called Shopee using Spam Classification and Sentiment Analysis with VinaLLaMA - a Vietnamese Large Language Model.

---

## 1. Data Gathering and preprocessing
Data is gathered using ExportComments.com. 
### Links:
- EXPORT COMMENTS:
  https://exportcomments.com/

Then, data is roughly cleaned and compiled using Pandas. Irrelevant features like index column, image and video URLs are dropped, row duplicates are removed, columns are renamed and new features like "Product name" and "Duplicated" are added.
