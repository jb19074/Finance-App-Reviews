
# Sentiment Analysis for Robo Advisors in Singapore

Analyzing the sentiment of user reviews for various Robo Advisor Apps in Singapore.

## Introduction

The rise of Robo Advisor Apps has provided an avenue for many to venture into investment platforms. User reviews are a goldmine of data that provides insights into the strengths and weaknesses of these platforms. However, navigating through a plethora of reviews to decipher general sentiment can be daunting. This project offers an analytical approach to understand users' likes and dislikes, thereby helping Robo Advisor companies and potential users declutter the noise of reviews.

## Data

**Source**: The data was sourced from Google Play Reviews through the Google Play Scraper.

**Description**: The dataset contains details such as:
- **reviewId**: Review Identifier
- **userName**: Username of the reviewer
- **userImage**: Profile picture of the reviewer
- **content**: The review content
- **score**: Rating out of 5
- **thumbsUpCount**: Number of thumbs up the review received
- **reviewCreatedVersion**: App version for which the review was written
- **at**: Datetime when the review was posted
- **replyContent**: Reply from the Robo Advisor (if any)
- **repliedAt**: Datetime when the Robo Advisor replied

**Cleaning and Preprocessing**: The raw review data was transformed into a Pandas dataframe. The content of reviews was consolidated, and irrelevant words were filtered out using StopWords.

## Technologies & Libraries Used

- **Language**: Python
- **Libraries**:
  - Pandas
  - Matplotlib
  - Wordcloud
  - google_play_scraper
  - nltk Vader_Sentiment lexicon
  - sklearn (specifically tsne/kmeans)

## Analysis & Findings

The analysis involved the creation of word clouds from the complete review data, positive review data, and negative review data. Further, tsne/kmeans were used to derive topics and create word clouds for these topic clusters.

Key Findings:

- A significant number of users pointed out issues related to updates causing the app to crash.
- App performance as a roboadvisor was another point of contention among users.
- On the positive side, many users appreciated the ease of use and how these robo advisors streamlined their entry into market investments.

## Future Improvements

While the analysis provides valuable insights into the sentiment of users, there's potential to dive deeper into topic analysis to capture nuanced opinions. An area that can be further refined is the granularity of topics. The challenge lies in deciphering overlapping sentiments and ensuring that individual topics represent distinct user opinions.

---
