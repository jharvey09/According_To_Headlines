# According To Headlines
_________________________________________________________________________________________________________________________________________________________________________________
### Decrypting Cryptocurrencies through Natural Language Processing (NLP):
![sentimental](https://user-images.githubusercontent.com/80294571/130220294-922756ad-9914-45f9-97c6-1bb5cba0bb97.jpeg)
In this project I will apply natural language processing to understand the sentiment in the latest article featuring Bitcoin &amp; Ethereum.
Also I will apply fundamental NLP techniques to better understand the other factors involved with the coin prices focusing on common words, phrases, organizations, and entites mentioned.
Questions encompassing the "sentiment" is; what are articles saying about different cryptocurrencies? What is the current public sentiment surrounding these coins? NewsApi and NLTK (Natural Language Tool Kit) library utilized.
Below is a list of the tasks that were used to accomplish the plots shown later in the presentation:
## Tasks:
1. Semtiment Analysis
2. Natural Lanuguage Processing
3. Name Entity Recognition
### Steps:
1. After setting my NewsAPI Key, the first step was to fetch Bitcoin & Ethereum news articles
2. Next was to create the Sentiment Scores DataFrame using a for-loop for Bitcoin
3. The same process was performed for Etherum. After converting to a DataFrame using pd.DataFrame
4. A ".describe()" function shows us important numbers related to the Sentiment Score
![image](https://user-images.githubusercontent.com/80294571/130223083-fc58c107-5dbe-44e5-b988-c59d45ac63f2.png)
_________________________________________________________________________________________________________________________________________________________________________________
### Questions:
Q: Which coin had the highest mean positive score?

A: Bitcoin with the score of 0.0519600

Q: Which coin had the highest compound score?

A: Bitcoin with the scotre of 0.8834000

Q. Which coin had the highest positive score?

A: Bitcoin with the score of 0.2740000
_________________________________________________________________________________________________________________________________________________________________________________

## Tokenizing:
### Steps:
1. Import NLTK (Natural Language ToolKit) nltk.tokenize, nltk.corpus, nltk.stem
2. Import Lemmatizer 
3. Import word_tokenize, sent_tokenize
4. Import WordNetLemmatizer, PorterStemmer
5. Now we can take a look at unique word counts
6. We can then use the imported Counter function to count the frequency of words in the articles
7. The top 3 most frequently used words in the Bitcoin news articles were "char" (95x), "Bitcoin" (49x) and "Reuters" (23x)
_________________________________________________________________________________________________________________________________________________________________________________

### WordCloud
Word clouds are an intuitive way to visualize the frequency of different words in a news article to quickly see which words were most prominently used. Word clouds are also very easily generated with Python
#### Bitcoin WordCloud
![image](https://user-images.githubusercontent.com/80294571/130224593-1d7aae1b-8734-47eb-852d-32d65b7d9a9f.png)

#### Ethereum WordCloud
![image](https://user-images.githubusercontent.com/80294571/130224887-8782a10a-1ea7-4748-ac2e-bea9bfc9e610.png)
_________________________________________________________________________________________________________________________________________________________________________________
## Name Entity Recognition [NER]:
NER generates visually-appealing text that makes it clear what words are important within the article, and to what "category" that word belongs to: is it an organization, a currency, a name, etc.
### Steps
1. Import Spacy
2. Concatenate all Bitcoin/Ethereum text together using the ".join()" function. 
3. Then, run NER processor on text, and render visualization

#### Input:
bitcoin_doc = nlp(bitcoin_text)
displacy.render(bitcoin_doc, style='ent')

#### Output:
![image](https://user-images.githubusercontent.com/80294571/130225658-40899c93-4a79-4a3e-bbf2-2a7afb225cab.png)





 






