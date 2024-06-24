# -Sentiment-Analysis
import nltk
from nltk.sentiment import SentimentIntensityAnalyzer

nltk.download('vader_lexicon')

sia = SentimentIntensityAnalyzer()

def analyze_sentiment(text):
  """Analyzes the sentiment of given text using VADER."""
  sentiment = sia.polarity_scores(text)
  return sentiment

# Example Usage:
review = "This restaurant is amazing! The food is delicious and the service is great."
sentiment = analyze_sentiment(review)
print(sentiment) 
