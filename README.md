# Social-Media-Electoral-Analytics
"To propose a series of metrics (analytical measures) derived from the various conversations and opinions expressed on Twitter-X concerning the three candidates for the 2024 presidential elections in Mexico."

With the aim and objectives of understanding whether these conversations on Twitter-X serve as a proxy for electoral preference. Additionally, to determine if the conversations on Twitter-X are a faithful representation of narrative patterns in electoral behavior. Most importantly, to initiate a dialogue regarding the reading, interpretation, and implications of such an analysis at the dawn of a presidential election."

Methodology

We have developed various metrics (analytical measures) based on three natural language processing models utilizing neural networks, which enable us to trace similarities, relationships, and approximations to electoral preferences derived from the discourse and commentary on Twitter-X.

The metrics we have developed are as follows:

• Sentiment Classifier:
Predicting whether a tweet is Positive, Negative, or Neutral regarding a particular candidate.

• Mobilization Classifier:
Predicting whether a tweet indicates participation and mobilization to vote for a specific candidate.

• Segmentation:
Grouping the various candidates based on certain meanings, semantically related words, and messages.

• Ideological Distance:
The difference (distance) between what a candidate articulates in their speeches and what is expressed in the tweets that mention them. A smaller distance signifies a greater closeness between the texts, that is, between what the candidate says and what the tweets convey.

• Preference:
A composite metric that averages the sentiment, participation or mobilization, and ideological distance metrics.

How?

Using a pre-trained Large Language Model (LLM) from the open-source platform HuggingFace (Robertuito), we automatically classified 7,349 tweets that mentioned any of the three presidential candidates into categories of Positive, Negative, and Neutral. Similarly, with another open-source algorithm called Roberta, we classified the texts based on whether they invited participation and mobilization for any of the candidates.

Manually, a team of three individuals classified an additional 3,000 tweets that mentioned any of the three presidential candidates into Positive, Negative, and Neutral categories.

With both the manual and automatic classifications, we calibrated the LLM to ensure the text classification was more pristine, clear, and reflective of the genuine sentiments, emotions, attitudes, and evaluations regarding the presidential candidates. This calibration was adapted to the semantic and syntactic localisms of Mexican Spanish.

Subsequently, we conducted an additional text cleaning process with extra classification criteria, such as including certain hashtags as negative or positive, as well as identifying frequent words with positive and negative connotations found in the manual classification. Similarly, we selected a series of additional words that signified support, participation, and mobilization for any of the candidates.

To calculate the ideological distance, we employed a metric called Cosine Similarity to determine how different two texts are. This provided us with a metric of difference between what the candidates say and what is expressed in the tweets.

Representativeness

One of the principal matters we must consider is that the representativeness of the universe we are portraying and analysing is limited. The foremost reason for this limitation is that the units of measurement are not individuals but rather unique Twitter-X accounts.

These units of measurement are not geographically nor sociodemographically representative of the population of Mexico. Nevertheless, we consider that they are indeed representative of the universe of unique accounts present on Twitter-X Mexico (17.5 million).

Thus, the sample universe we seek to represent is as follows:

• Sample: 300 tweets daily from the 18th of March until the 3rd of June.
• Randomness: Downloads at various hours of the day, adhering to the criterion that they be unique accounts, minimising the incidence of Bots and excluding retweets.


Sources: 

https://arxiv.org/abs/2111.09453

https://huggingface.co/pysentimiento/robertuito-sentiment-analysis

https://huggingface.co/bertin-project/bertin-roberta-base-spanish

https://github.com/pysentimiento/robertuito










