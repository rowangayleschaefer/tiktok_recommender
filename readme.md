#### TikTok Video Recommender

This is a truncated version of my final capstone project; repo only includes modeling steps and data used for modeling. 

Data acquisition, cleaning, and anaylsis sections have not been included in this repo.

<br /><p>

#### Data

Trending data by For You Page (FYP) location was scraped from TikTok using Tiktok-All-In-One from FastApi.

<br /><p>

#### Overview

For this project, I built a video recommender system using SpaCy. 

Unique preprocessing steps included building out a dictionary of Gen-Z/social media-specific stopwords to reduce "noise" in the data, and preserving hashtags and @ symbol in word lemmatization.

Final model recommends videos based on lemmatized video description text and hashtags included in description.

<br /><p>

Next steps:
    
* Adding post author, FYP location, origin country of video, and song title/artist to recommender. 
    
* Building a model that returns relevant videos based on user entry (textbox) or dropdown selection of their interests.
    
* Web app that allows user to enter interests, and plays relevant videos.
    
* Do an API pull for videos; see how closely tiktok's list of recommended (similar) videos matches mine.
    
    
<br /><p>
  
Ideas to improve performance:
   
* I would like to find a model that was trained on social media (twitter or instagram). Despite returning videos with relevant descriptions, this recommender misses some connections due to issues understanding and comparing compound words.
   
* (a test of models that were built for cosine similarity showed that they did not include support for parsing compound words - i.e. most compound hashtags "#irishhumor" had a low similarity score when comparing to hashtag "irish".)
    
* Adding another layer (?) of meaning by using nlp on description text, then comparing word vectors to build recommender. This might help with homonym issues and returning videos by similar overarching categories. I attempted this when building an earlier version of the model, but do not know if it is possible. 
