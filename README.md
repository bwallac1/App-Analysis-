# Utilizing Sentiment Analysis to do Comparative App Analysis  

##Motivation

I was seeking to understand how can we identify apps that are seen as most effective for learning CS education topics such as programming. The most common apporach to this is sentiment analysis 

Parsing and analyzing app review data is a common practice for developers seeking to enhance their mobile applications and better meet user needs. 

This data, sourced directly from users, offers valuable insights into user sentiment and experiences. It provides developers with direct feedback on areas for improvement, pain points, and well-received features. 

However, a key question arises: Are current methods for analyzing this data and its sentiment effectively capturing the nuances present within?

###Understanding Sentiment: Definitions and Importance

What is Sentiment?

Sentiment refers to the emotional tone or attitude expressed in text data. It can be positive, negative, or neutral.

Why is it Important?

Sentiment analysis helps businesses, researchers, and individuals gain insights into public opinion, customer satisfaction, and brand perception.

###Lexicon-Based Approaches: Strengths and Limitations

Strengths

Lexicon-based methods are simple, fast, and easy to implement. They rely on pre-defined lists of words with associated sentiment scores.

Limitations

These approaches may struggle with sarcasm, irony, and context-dependent sentiment.


Machine Learning(ML) Approaches: Strengths and Limitations

Strengths

ML algorithms, such as Support Vector Machines (SVM), Naive Bayes, and deep learning models like Convolutional Neural Networks (CNNs) and Recurrent Neural Networks (RNNs), can be trained on labeled datasets to classify sentiment.

ML approaches can be more adaptable and handle complex language,

Hybrid Approaches: Strengths and Limitations

Strengths

These methods combine the strengths of lexicon-based and ML approaches.[9] 

They may use lexicon-based techniques for initial sentiment scoring and then apply ML algorithms for refinement.


##Related Work in Sentiment Analysis 

Aspect-Based Sentiment Analysis (ABSA): ABSA emerges as a powerful tool to analyze user reviews by identifying sentiment towards specific features or aspects of an app. This goes beyond simply gauging overall sentiment (positive, negative, neutral) and provides granular insights into what users like or dislike about specific aspects.

Pranatawijaya et al. (2024) demonstrate the effectiveness of combining ABSA with powerful language models like BERT to achieve high accuracy in sentiment classification (97%). They also highlight the importance of addressing unbalanced datasets using techniques like SMOTE to ensure reliable results.

Bahri and Suadaa (2023) applied IndoBERT for ABSA on Google Maps reviews of the Bromo Tengger Semeru National Park, finding that attractions, amenities, and pricing were the most frequently mentioned aspects.

##Research Questions

Can sentiment analysis methodologies be extended utilizing ChatGPT to provide a more nuanced analysis of apps used for learning programming?

What features do reviewers identify as providing the most satisfaction?

What frustrations are highlighted across apps that are intended for learning programming through?


##Methods

For this project I completed sentiment analysis on 5 target CS education apps for learning programming in two comparing the efficacy and results.  

Data Collection: Collect user reviews for target CS applications from the App Store. 150 reviews will be analyzed from each app. 

Sentiment Analysis: Conduct sentiment analysis on the target app reviews utilizing to distinct methods to compare compare

First method: Traditional sentiment analysis utilizing available NLTK Libraries alone, in particular I utilized the RoBERTa algorithm (twitter-roberta-base-sentiment) that is has been designed specifically for social texts. 

Second Method: Utilizing LLM, in particular Chat GPT agents trained on Sentiment analysis documentation.

Method Comparison: Complete a comparative analysis of results from each method accounting for alignment and gaps. 

Target Apps: All these apps are comparable in approach to teaching programming such as python. 
1.Codecademy Go
2.Mimo
3.Kodable 
4.Encode 
5.Codea 

##Results
See Presentation ( for LLM  Results) https://gamma.app/docs/Utilizing-Sentiment-Analysis-to-do-Comparative-App-Analysis--45dxj6tuq7ym0um
See Competitive App Analysis Notebook ( for Traditional Approach Results) 


##Findings 

Utilizing LLM (ChatGPT) trained to do senitiment analysis provided additional contextual nuance in analysis and results

The LLM approch results was able to process results with accountaing for things such as irony,sarcasm, etcc with isse provide a way to ameliorate possible miscategorizations of reviews. 

The two approaches provided similar results in the pure labeling of reviews showing that most of this is attribituted to the library utilized to train the LLM aand complete analysis. However the LLM approach provide additional insights that the traditional method did not. 

Overall users really enjoyed gamification in learning code and those apps that include it showed higher positive sentiments even if other features were not as appreciated. 

Most frustration points accross apps included issues with stability, cost and limited features. 


##Limitations

In working with both methods some limitations arise: 

Traditional Method: Issues discerning context dependent situations, must be trained to for large sets of vocabulary and can be costly in computation, for results that can offer simple analysis and coding of data only without addition helper applications to process insights and visualizations. 

LLM Method: Much of the interpretation is left up to the the LLM which provides for opportunities of concern to arise based on with versions and models are utilized. Training the model still has to occur utilizing a ML sentiment analysis algorithm and so the method can also be computationally costly. 



##Insights

I believe utilizing LLMs such as ChatGPT can provide additional insights that have been more difficult to obtain using traditional methods. While this project involved a small number of sentiments compared to others, it consistently showed that the LLM approach yielded similar labeling outcomes and provided synthesis beyond literal context.

I would be interested in seeing this approach used more often as it becomes a validated option for sentiment analysis. The method is similar to hybrid approaches already in use and has the potential to maximize the potential of sentiment analysis for user reviews, particularly as LLMs become more agile.

Through comparative analysis of the five target apps, I found that users are most likely to be satisfied with coding apps that provide some form of gamification, leveling up, advanced features, and are low- or no-cost.

I also ascertained that users are most concerned with having an app that runs smoothly without issues and offers flexibility between mobile and desktop use.


##Challenges and Future Directions in Sentiment Analysis

Contextual Understanding: Improving the ability to understand sentiment in context, including sarcasm, irony, and cultural nuances.

Cross-Lingual Analysis: Developing methods to accurately analyze sentiment in different languages, overcoming linguistic barriers.

Data Privacy and Ethics: Addressing privacy concerns and ethical considerations when analyzing sensitive or personal data.

Challenges and Future Directions in Sentiment Analysis

Contextual Understanding

Improving the ability to understand sentiment in context, including sarcasm, irony, and cultural nuances.

Cross-Lingual Analysis

Developing methods to accurately analyze sentiment in different languages, overcoming linguistic barriers.

Data Privacy and Ethics

Addressing privacy concerns and ethical considerations when analyzing sensitive or personal data.

##References 

Pranatawijaya, V. H., Sari, N. N. K., Rahman, R. A., Christian, E., & Geges, S. (2024). Unveiling User Sentiment: Aspect-Based Analysis and Topic Modeling of Ride-Hailing and Google Play App Reviews. Journal of Information Systems Engineering and Business Intelligence, 10(3), 328–339). https://doi.org/10.20473/jisebi.10.3.328-339

Nakayama, M., & Wan, Y. (2019). Cross-Cultural Examination on Content Bias and Helpfulness of Online Reviews : Sentiment Balance at the Aspect Level for a Subjective Good. In HICSS 52 (Vol. 6, pp. 1154–1163).

Subekti, I., & Septianto, R. D. (2023). E-Service Quality Analysis for Video Players and Editor App Using Sentiment Analysis and Topic Modeling. Journal of Information Systems Engineering and Business Intelligence, 10(2), 252–262. https://doi.org/10.20473/jisebi.10.2.252-262

Haering, M., Bano, M., Zowghi, D., Kearney, M., & Maalej, W. (2021). Automating the evaluation of education apps with app store data. IEEE Transactions on Learning Technologies, 14(1), 16–27. https://doi.org/10.1109/TLT.2021.3055121

Massenon, R., Gambo, I., Ogundokun, R. O., Ogundepo, E. A., Srivastava, S., Agarwal, S., & Pak, W. (2024). Mobile app review analysis for software requirements elicitation: a systematic mapping study. PeerJ Computer Science, 10, 2401. 







