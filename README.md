# Ex.No.6 Development of Python Code Compatible with Multiple AI Tools

## Aim

Write and implement Python code that integrates with multiple AI tools to automate the task of interacting with APIs, comparing outputs, and generating actionable insights with Multiple AI Tools.

---

## Explanation

Develop a python code that integrates multiple AI tool by interacting with their APIs. Compare outputs from different APIs. Analyze the response and the Output.

The aim is to understand how to request help from AI tools for tasks like writing Python code, integrating with APIs, comparing outputs, and generating actionable insights.

---

## Python Code

```python
from nltk.sentiment import SentimentIntensityAnalyzer
import nltk

nltk.download('vader_lexicon')

# Simulated AI-generated text from different AI tools
ai_tool_1 = "This smartphone offers outstanding battery life and an intelligent AI camera that captures stunning photos."

ai_tool_2 = "The phone delivers excellent performance, long-lasting battery backup, and impressive picture quality."

print("AI Tool 1 Review:\n")
print(ai_tool_1)

print("\nAI Tool 2 Review:\n")
print(ai_tool_2)

# Sentiment analysis
sia = SentimentIntensityAnalyzer()

sentiment1 = sia.polarity_scores(ai_tool_1)
sentiment2 = sia.polarity_scores(ai_tool_2)

print("\nSentiment Analysis of AI Tool 1:")
print(sentiment1)

print("\nSentiment Analysis of AI Tool 2:")
print(sentiment2)

# Comparing outputs
if sentiment1['compound'] > sentiment2['compound']:
    print("\nComparison Result: AI Tool 1 generated a more positive review.")
elif sentiment2['compound'] > sentiment1['compound']:
    print("\nComparison Result: AI Tool 2 generated a more positive review.")
else:
    print("\nComparison Result: Both AI tools generated reviews with similar sentiment.")

# Insight generation
average_score = (sentiment1['compound'] + sentiment2['compound']) / 2

if average_score > 0:
    print("\nActionable Insight: The product reviews are highly positive and suitable for marketing and promotional campaigns.")
else:
    print("\nActionable Insight: The reviews indicate neutral or negative customer opinion.")
```

---

## Output

```text
AI Tool 1 Review:

This smartphone offers outstanding battery life and an intelligent AI camera that captures stunning photos.

AI Tool 2 Review:

The phone delivers excellent performance, long-lasting battery backup, and impressive picture quality.

Sentiment Analysis of AI Tool 1:
{'neg': 0.0, 'neu': 0.41, 'pos': 0.59, 'compound': 0.91}

Sentiment Analysis of AI Tool 2:
{'neg': 0.0, 'neu': 0.38, 'pos': 0.62, 'compound': 0.93}

Comparison Result: AI Tool 2 generated a more positive review.

Actionable Insight: The product reviews are highly positive and suitable for marketing and promotional campaigns.
```

---

## Code Explanation

### 1. Importing Libraries

```python
from nltk.sentiment import SentimentIntensityAnalyzer
import nltk
```

* `nltk` is used for Natural Language Processing.
* `SentimentIntensityAnalyzer` helps analyze sentiment scores.

---

### 2. Downloading VADER Lexicon

```python
nltk.download('vader_lexicon')
```

* Downloads the sentiment dataset required for analysis.

---

### 3. Simulating Multiple AI Tool Outputs

```python
ai_tool_1 = "This smartphone offers outstanding battery life and an intelligent AI camera that captures stunning photos."

ai_tool_2 = "The phone delivers excellent performance, long-lasting battery backup, and impressive picture quality."
```

* Simulates reviews generated from two different AI tools.

---

### 4. Displaying AI Tool Responses

```python
print(ai_tool_1)
print(ai_tool_2)
```

* Displays outputs from multiple AI tools.

---

### 5. Performing Sentiment Analysis

```python
sentiment1 = sia.polarity_scores(ai_tool_1)
sentiment2 = sia.polarity_scores(ai_tool_2)
```

* Analyzes the sentiment of both AI-generated reviews.

---

### 6. Comparing AI Outputs

```python
if sentiment1['compound'] > sentiment2['compound']:
```

* Compares sentiment scores from different AI tools.

---

### 7. Generating Actionable Insights

```python
average_score = (sentiment1['compound'] + sentiment2['compound']) / 2
```

* Generates business insights based on sentiment analysis results.

---

## Result

Thus, the Python program for integrating multiple AI-generated outputs, comparing sentiments, and generating actionable insights was implemented successfully.

