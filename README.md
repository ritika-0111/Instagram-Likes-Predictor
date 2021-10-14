# Instagram-Likes-Predictor
Dataset used in this repository contains data of 16539 rows with 20 feature columns, they are as follows:

* numberPosts  
* website  
* urlProfile  
* username  
* numberFollowing  
* descriptionProfile  
* alias  
* numberFollowers  
* urlImgProfile  
* filename  
* date  
* urlImage  
* mentions  
* multipleImage  
* isVideo  
* localization  
* tags  
* numberLikes  
* url  
* description  

# Approach:
 1) Explore Dataset and get rid of additional and less useful features
 2) Consider given features like numberPosts, numberFollowing and numberFollowers.
 3) Extract some possible features like 
     * Website: we have classified the website provided in the user description into different categories: Youtube, Music, Tumblr, Facebook, Blog, Twitter and other. Then we one-hot-encode the different categories.
     * Day of the week: using the data of each data post and then we one hot encoded the day of the week  
 4) Applying an XGBoost model on these features.
 
# Result Obtained:
   ![Screenshot (270)](https://user-images.githubusercontent.com/51761546/137395264-407e9fcd-7d59-4961-91aa-26ffb9bfb6e3.png)
   
# Future Scope:
  1) NLP: In our data set there were some text data that we can use as well like 
     * User's bio: It contains information that users write to give their intro and about the content of the profile
     * Caption mentioned in each post: Along with textual data at times it also contains hashtags.
     * location: Location of the post creation.
  3) Transfer learning: To identify features related to images that may be meaningful in determining the final number of likes. This can be done in the following way- 
     * Fine-tuning the ConvNet with Inception V3
     * Fixed feature extractor with VGG 19 
  4) Convolutional Regression Neural Network: We can analyze image data of the Instagram Post being posted.
  
