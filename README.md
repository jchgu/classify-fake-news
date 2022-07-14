# Overview

How to detect "fake news" content that is intended to mislead the audience? To quickly identify and classify fake news on a large scale, novel techniques like machine learning can come into use. My classmate Sarah Sramota and I trained a basic Naive Bayes classifier to predict the credibility of news articles. Sarah implemented the code and I wrote up the findings. This was an assignment for the tutorial [Supervised Text Classification](https://github.com/ccs-amsterdam/r-course-material/blob/master/tutorials/r_text_ml.md#training-the-model-using-quanteda) by [@ccs-amsterdam](https://github.com/ccs-amsterdam) in January 2021. One year and a half later, I updated the code to be compatible with the latest R pacakges.

# Data Availability and Provenance Statements

We chose the [ISOT Fake News Dataset](https://www.uvic.ca/ecs/ece/isot/datasets/fake-news/index.php) compiled by Ahmed, Traore, and Saad (2018, 2017). The compilation consists of two datasets: The Real News Set contains 21,417 pieces of real news and the Fake News Set 23,481 pieces. Each article includes the title, full-text, and the publishing date. Most articles feature (American) political and international news between 2016 and 2017. The reliable news articles were collected from the Reuters website. The fake news articles were gathered from various websites that [Politifact](https://www.politifact.com/) marked as untrustworthy. The articles in the dataset were labelled.

## Statement about Rights

I certify that the authors have legitimate access to and permission to use the data. 

## Summary of Availability

All data are publicly available.

## Dataset list

| Data files  | Source | Notes               | Provided |
| ----------------- | ------ | ------------------- | -------- |
| `Fake.csv` `Real.csv` | [ISOT Lab](https://www.uvic.ca/ecs/ece/isot/datasets/fake-news/index.php)  |  | Yes (in the external site) |

# Computational requirements

I adopt `R` (version 4.2.0) for all the analyses. This involves the following packages:
`quanteda` (3.2.0), `quanteda.textmodels` (0.9.4), `quanteda.textplots` (0.94.1), `quanteda.textstats` (0.95), `readr` (2.1.2), `lexicon` (1.2.1)

## Memory and Runtime 

Less than ten minutes is needed to reproduce the analyses on a standard 2022 desktop machine. This does not account for Chunk 37, which takes a long time to run. The code was last run on a Windows 11 laptop with a 4-core Intel processor. 

# Instructions to Replicators

Download `Real.csv` and `Fake.csv` from the [ISOT Lab](https://www.uvic.ca/ecs/ece/isot/datasets/fake-news/index.php), and `script_classify_fake_news.Rmd` from this depository. Place them in the same folder. Run the script to execute all steps in sequence. 

# Reference

Ahmed, H., Traore, I., & Saad, S. (2018). Detecting opinion spams and fake news using text classification. *Security and Privacy, 1*(1), e9. https://doi.org/10.1002/spy2.9

Ahmed, H., Traore, I., & Saad, S. (2017). Detection of Online Fake News Using N-Gram Analysis and Machine Learning Techniques. In I. Traore, I. Woungang, & A. Awad (Eds.), *Intelligent, Secure, and Dependable Systems in Distributed and Cloud Environments* (pp. 127–138). Springer International Publishing. https://doi.org/10.1007/978-3-319-69155-8_9
