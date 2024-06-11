# NLP-Based Sentiment Dissection of Apple Vision Pro Reception on Marques Brownlee’s YouTube Channel.
![image](https://github.com/ashleySimiyu/Capstone-Project/assets/141912273/8c100e2d-e343-4f56-99b8-9c1c247f0fec)

## Business Understanding
### Project Overview
The Apple Vision Pro, a cutting-edge product in the realm of augmented reality, has garnered significant attention since its release. As a prominent influencer in the tech community, Marques Brownlee's reviews on YouTube significantly impact consumer perceptions and purchasing decisions. Given this influence, there's a substantial interest from Apple’s product development and marketing teams to understand public sentiment as expressed in the comments on these review videos.

### Business Problem
The project aims to analyze viewer comments on Marques Brownlee's YouTube channel related to the Apple Vision Pro. By using Natural Language Processing (NLP) techniques, the project seeks to understand the sentiments expressed in the comments and identify whether viewers are inclined towards purchasing the product. The insights gained from this analysis will help the Product Development Team at Apple assess the reception of the Apple Vision Pro among Marques Brownlee's audience

### Objectives
Our main objective of this study is to analyze viewer sentiments in comments on Marques Brownlee’s YouTube videos reviewing the Apple Vision Pro product.
  * Other Objectives are:
1. Purchase Intent Analysis: Determine the likelihood of viewers purchasing the Apple Vision Pro based on their comments.
2. Insights Generation: Provide actionable insights to the Product Development Team at Apple regarding the reception of the Apple Vision Pro among Marques Brownlee's viewers.
3. Report Preparation: Create a detailed report summarizing the findings and recommendations for further action.
   
**The primary stakeholders are the product development team, marketing team, and strategic decision-makers at Apple.**

### Research Questions
1. What are the top 10 viewed videos on Marques Brownlee's Channel?
2. Can sentiments expressed in comments predict a viewer’s likelihood to purchase the Apple Vision Pro? (based on positive, negative sentiments).
3. How are sentiments distributed across comments on Marques Brownlee's YouTube videos reviewing the Apple Vision Pro?
4. Leveraging on the historical data gathered can Apple Vision Pro Production team improve their marketing strategy?
5. What are the predominant themes?key words and sentiments expressed in viewer comments on Marques Brownlee’s YouTube videos?
   
## Data Understanding
The data for this project consists of comments from Marques Brownlee's YouTube channel related to the Apple Vision Pro review videos. The comments are collected using the **YouTube Data API**, which allows access to public comments on YouTube videos. Each comment is associated with metadata such as the commenter's username, comment timestamp, comment text, and number of likes. The comments provide insights into viewers' opinions, feedback, and preferences regarding the Apple Vision Pro product. The comments will be preprocessed to remove special characters, stopwords, tokenize the text, lemmatize and perform sentiment analysis using NLP techniques.
* We first install the Python packages using pip
> %pip install --upgrade google-api-python-client

> %!pip install textblob
* We then Set up our YouTube Data API
  
![Screenshot (43)](https://github.com/ashleySimiyu/Capstone-Project/assets/141912273/b5a0c23f-8ffb-4a80-bf1f-0a62a1182f5c)
 * We checked the top 10 most viewed videos done by Marques Brownlee, and these were the results which included The Apple Vision Pro product.

![Top 10 Videos by Views](https://github.com/ashleySimiyu/Capstone-Project/assets/141912273/ef454237-87c6-4d94-9565-dfe64e2721f1)

 * From the chart,here were two videos featuring the Apple Vision Pro product.. We combined the two videos to create a dataset that would be used for analysis.    
### Data Structure
  * Data Format: CSV
  * Number of rows = 59,274
  * Number ofcolumns = 4
###  Data Features 
  * Comment Text
  * Likes (Number of likes on the comment)
  * Author (The username of the author that made a comment)
  * Timestamp (Time the comment was posted)
### Data Types
  * Comment text: String
  * Likes: Integer
  * Author: String
  * Timestamp: DateTime
### Data Cleaning
1. **Emoji and Non-English Word Removal:** Emojis and non-English words were removed from the comments as they were considered noise. Any comment containing only emojis or non-English words was treated as an empty row and removed from the dataset.
2. **Tokenization:** The comments were tokenized, splitting them into individual words or tokens. This step is essential for further analysis as it breaks down the text into manageable units.
3. **Stopwords removal:** Removing stopwords helps reduce noise in the data and focuses the analysis on more meaningful words.
4. **Lemmatization:** Lemmatization was applied to the tokens to reduce them to their base or root form. 

## Modelling 
We are using Natural Language Processing (NLP) techniques to analyze the sentiments expressed in the comments.
These are the results:
### 1. Textblob Model
**Average Polarity:** 0.07427583991647495
This positive value, although close to zero, indicates a slight overall positive sentiment across all the comments analyzed. This suggests that, on average, the comments tend to be more positive than negative, but only marginally so.
**Average Subjectivity:** 0.38530032477277043
This value is closer to 0 than to 1, suggesting that the comments, on average, tend to be somewhat objective. However, there is still a significant presence of personal opinions and subjectivity in the data.
![Uploading Sentiment Distribution - TextBlob Model.png…]()

### 2. VADER Model
**Average VADER Sentiment:** 0.16775339665611289
![Uploading VADER sentiment Distribution.png…]()

### 3. SUPPORT VECTOR MACHINES (SVM) Model
**Accuracy:** 0.9141825587854101
The model does a good job in correctly identifying Positive sentiments, with a high count of true positives.However, the model struggles more with misclassifying Negative sentiments as Positive, and vice versa, which could be due to overlapping language cues used in Negative and Positive sentiments.

### 4. Long Short-Term Memory (LSTM) Model
With a low log loss of 0.436 and a high accuracy of approximately 92.37% on the test dataset indicates that the model has performed better
## Conclusion
In conclusion, the project provides a solid foundation for enhancing marketing strategies by utilizing key words that have positive sentiment scores. This project shows that Apple can track how to gain more clients or customers by incoporating NLP analysis. 

The Apple Production Team can target different demographics responses to Apple Vision Pro product and monitor how it transitions to increase or decrease in their sales revenue. Therefore,they can develop and implement data-driven strategies aimed at improving customer satisfaction, and ultimately increase sales of such products.

## Recommendations
- **Product Development:** Use insights from sentiment analysis to guide the Apple Vision Pro product development and improvement. Features of the prodcut are consistently viewed negatively, these areas could be prioritized for upgrades.

- **Marketing Strategies:** Adjust marketing strategies based on the sentiments expressed. For products receiving positive sentiments, highlight these aspects in marketing campaigns.

- **Customer Service:** Implement findings to improve customer service by addressing common complaints or queries that arise in sentiment analysis.

## Next Steps
**Expand Training Data:** Incorporate more data from other sources or additional YouTube channels to improve the model's robustness and generalizability.

**Cross-Platform Analysis:** Expand the analysis to include data from other social media platforms like Twitter, Facebook, or Instagram to gain a more comprehensive view of public sentiment.

**Demographic Analysis:** If possible, analyze sentiments across different demographics to tailor products or marketing more effectively to specific groups.
# Applesight-analyzing-youtube-comments-on-apple-visionpro
