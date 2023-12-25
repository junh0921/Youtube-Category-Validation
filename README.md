
# Youtube Category Validation

### Data Collection 
Collected Dataset containing US / GB Trending Youtube videos' statistics from Kaggle - [Dataset](https://www.kaggle.com/code/anshikatanya/data-analysis-on-youtube-trending-videos)


### Proposal

Hypothesis: YouTube’s current 16 categories may not be the best way to represent video content accurately

* Initial Observations: Analysis of JSON file category names revealed overlaps and similarities. 
    * (e.g. ‘VideoBlogging’ and ‘People & Blogs’ / ‘Entertainment’, ‘Comedy’ and ‘Gaming’)
➡️ Raised questions about the need and distinctiveness of all 16 categories

* Textual Analysis: Examined video/channel titles, tags, and comments, without viewing the videos and found instances of similar videos categorized differently
➡️ This discrepancy casts doubt on the adequacy of the current categorization



### Process 

* Processed and transformed the dataset containing US Youtube videos’ statistics by one-hot encoding, vectorizing and normalizing data using Python pandas and scikit-learn
* Applied K-means clustering and elbow method using scikit-learn to identify whether the optimal number of categories match current number of categories
* Utilized google gensim word2vec model to find which current category pairs yield high similarity scores


### Results
Based on our result from Clustering, Elbow Method, and Silhouette score, we have identified that the current number of categories is not ideal. The K that yielded the highest silhouette score turned out to be 5, which is a significant difference from the original. To test whether this result is reliable, we conducted another test using a word similarity model and discovered many of the category names are very similar to one another.

<img width="692" alt="Screen Shot 2023-12-25 at 6 38 28 PM" src="https://github.com/junh0921/Youtube-Category-Validation/assets/107960371/5dc47130-429e-42a2-835c-76dc3989ff5b">
<img width="289" alt="Screen Shot 2023-12-25 at 6 39 20 PM" src="https://github.com/junh0921/Youtube-Category-Validation/assets/107960371/6ec7e607-79c9-4dc9-b5d2-83668895fd0e">

