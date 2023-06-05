# 13. Classification of Comments.
Online store launches new service allowing users to edit and supplement product descriptions, similar to wiki communities (clients can propose edits and comment on others' changes). To ensure a safe environment, the store requires a tool to detect toxic comments for moderation.

[HTML](13_toxic-comments.html)   [ipynb](13_toxic-comments.ipynb)

### Goal: 
Develop an ML model to classify comments into toxic and neutral.<br>
Target performance metric: **F1 >= 0.75**.
### Data: 
A collection of marked comments indicating toxicity level (0 for neutral comments, 1 for toxic comments).
### Framework:
-	Data overview and preprocessing: cleaning texts, lemmatization.
-	WordClouds for toxic and neutral comments.
-	Pipeline incorporating TF-IDF vectorization and model selection.
-	Model testing, WordClouds of words predicted as toxic or neutral
-	General conclusion.
### Result:
The texts of comments were vectorized using TF-IDF after undergoing lemmatization with pos-tagging.<br> 
*Models tested*: `LogisticRegression`, `LGBMClassifier`, `LinearSVC` with different TF-IDF parameters.<br>
*The best-performing model*: `LinearSVC`, **F1 = 0.79** on the test set. This score was obtained without employing class weight balancing, utilizing only unigrams, and ignoring words with a document frequency < 0.1 and > 0.5.<br> 
Graphical representation of the classification outcome through WordClouds further confirmed the model's effectiveness.
### Stack: 
- `Pandas`, `Matplotlib`, `Seaborn`, `NumPy`, `Scikit-learn`, `NLTK`
-  *WordNetLemmatizer, pos-tagging, TF-IDF*
-  *LogisticRegression, LGBMClassifier, LinearSVC*
-  *Pipline, WordCloud*
