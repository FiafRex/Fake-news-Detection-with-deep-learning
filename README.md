Fake News Detection with Deep Learning
Detect fake news articles by leveraging deep learning techniques. This project identifies specific keywords from news articles and compares them against a dataset sourced from Kaggle, achieving an average accuracy of approximately 90%.

📊 Analysis
Word Clouds Comparison
Visualize the frequency of words in real vs. fake news.
Real news often cites specific publications, while fake news lacks these mentions.
Key findings:
Presence of "WASHINGTON (REUTERS)" in genuine articles.
Occurrence of tweets in the dataset.
Absence of publication info in some texts.
🧹 Data Cleaning
Extract and remove mentions like Reuters or tweets.
Separate publication details from the main content.
Filter out articles without any text.
Store the text and title in respective datasets.
🔄 Data Preprocessing
Assign class labels: real and fake.
Merge real and fake news datasets with their text and class.
📈 Vectorization with Word2Vec
Transform text data into numeric vectors.
Capture word context for semantic and syntactic similarity.
Use these vectors as initial inputs for machine learning models.
🚀 Testing the Model
To evaluate the model:

Copy a news summary or dataset into the x=[] field at the end of the code.
Execute the program.
Sample articles for testing:

DGCA lifts mask mandate
China eases COVID curbs
Neurological damage by COVID-19
🛠 Modules Used
NumPy: Efficient array operations.
Pandas: High-performance data analysis.
Matplotlib: 2D array plotting.
wordcloud: Visualize text data.
TENSORFLOW: Machine learning platform with high-level APIs.
