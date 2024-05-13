<H3>ENTER YOUR NAME : BARATHRAJ B S</H3>
<H3>ENTER YOUR REGISTER NO : 212222230019</H3>
<H1 Align="center">Project Based Experiment<H1>

### Objective:

Perform sentiment analysis using your Facebook data and filter the data that has only negative feedback for the code given in the following link.
  
### Program:
```
pip install pandas textblob
import pandas as pd
from textblob import TextBlob

# Load the CSV file into a DataFrame
df = pd.read_csv('fb_sentiment.csv')

# Function to perform sentiment analysis using TextBlob
def analyze_sentiment(text):
    blob = TextBlob(str(text))
    return blob.sentiment.polarity

# Apply sentiment analysis to each row in the DataFrame
df['Sentiment'] = df['FBPost'].apply(analyze_sentiment)

# Output the DataFrame with sentiment analysis results
print(df.head())

# Filter out rows with negative sentiment (label 'N')
negative_feedback = df[df['Label'] == 'N']

# Output the negative feedback
print(negative_feedback)

```
### Output: 
![image](https://github.com/Nivetham1710/Project-Based-Experiment-AAI/assets/94155183/34fecc73-ca7a-4869-9cf2-81d55058cfe7)

![image](https://github.com/Nivetham1710/Project-Based-Experiment-AAI/assets/94155183/3e25a40f-e35b-46d8-a513-9ba2d45fa13c)

### Inference:
Thus sentiment analysis using your Facebook data ias done and filtering the data that has only negative feedback for the code is done.
