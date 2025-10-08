# Project_CyberBullyingDectection
## Motivation:
Cyberbullying involves using the internet, mobile devices, or apps to harass, intimidate, or threaten others. It has become a widespread issue, affecting both children and adults. The consequences can be severe—ranging from emotional distress, anxiety, and depression to, in extreme cases, self-harm. Given the harmful impact of cyberbullying, it is essential to develop intelligent systems capable of detecting and preventing such behavior online. Machine learning provides a powerful means to identify bullying messages and help create safer digital spaces for everyone.

## Problem statement:
Cyberbullying detection systems utilize advanced machine learning models to recognize harassment, hate speech, and threats across online platforms. While existing models have significantly improved detection accuracy, key challenges persist. These include understanding contextual nuances, detecting sarcasm, and handling multilingual or code-mixed content—all of which often lead to misclassifications. To address these challenges, our system integrates the following components:
Detection: Leverages fine-tuned transformer-based models (like BERT) to accurately flag harmful content in text.
Mitigation: Minimizes the impact of identified cyberbullying by masking offensive text and tagging it as bullying, thus preventing its spread.
Continuous Learning: Incorporates user feedback to correct model predictions and incrementally retrains the model. 

## Related Works:
1. Social Media Cyberbullying Detection using Machine Learning [link]
This paper proposes several supervised learning models for detecting cyberbullying. It also shows that neural network classifiers perform better than SVM.
2. Machine Learning Approaches for Cyberbullying Detection [link]
This paper analyzes the combination of some NLP algorithms with machine learning to detect cyberbullying on Twitter. It indicates that the Extreme Gradient Boosting (XGBoost) model emerges as the best-performing classifier irrespective of whether it uses features from bag-of-words or TF -IDF
3. Cyberbully Detection Using BERT with Augmented Texts [link]
In this paper, we propose an architecture called Augmented BERT, which combines both data augmentation techniques and BERT for detecting cyberbullying content in texts. They propose to use various GAN-based and autoencoder-based data augmentation techniques to generate annotated data, which in turn is used to fine-tune BERT. 
4. Aggression Detection in Social Media from Textual Data Using Deep Learning Models [link]
This paper states that NLP-based extractors don’t consider the emotional context. They proposed a DNN model that was fed with a combination of embedded words and 8 different emotional features.
5. Utilizing Machine Learning for Detecting Cyberbullying in Social Media [link]
This paper shows how to detect cyberbullying using an SVM model on Twitter data.

## Method(s):
1. Data Collection: 
We utilized the Cyberbullying Classification Dataset from Kaggle, which contains tweet texts labeled across multiple categories of cyberbullying: religion, age, ethnicity, gender, and not_cyberbullying.
2. Pre-processing Techniques: 
Removed stopwords using the NLTK library.
Replaced slang terms with their full forms or contextual meanings.
Cleaned the text by removing special characters and numerical digits.
Encoded sentiment labels into numeric form for model training.
Tokenized the input text using BERT Tokenizer to prepare it for the transformer model.
3. Models:
Implemented a neural network-based solution using BERT (Bidirectional Encoder Representations from Transformers), a pre-trained transformer model fine-tuned for our multi-class classification task.
Designing the system to support a feedback loop, where user corrections (e.g., flagging incorrect predictions) are stored and later used to incrementally retrain the model.
Adding a mitigation layer that masks harmful content when bullying is detected reduces the negative impact of offensive messages.

