# Stress Detection Model Using NLP

This project demonstrates how to build a stress detection model using natural language processing (NLP) and machine learning techniques. The model classifies text as either "Stress" or "No Stress" based on its content.

## Project Overview
The project involves:
1. Data preprocessing (cleaning and stemming).
2. Visualizing text data using WordCloud.
3. Training a Naive Bayes classifier to detect stress in text inputs.
4. Using the trained model to classify user input in real-time.

## Installation

Ensure you have Python installed. Install the required dependencies using:

```bash
pip install pandas numpy nltk matplotlib wordcloud scikit-learn
```

## Dataset
The dataset contains Reddit posts labeled as "Stress" (1) or "No Stress" (0). Example columns include:
- `subreddit`
- `text`
- `label`

The dataset is loaded from a CSV file named `stress.csv`.

## Key Components

### Data Preprocessing
The `clean` function removes:
- HTML tags
- URLs
- Numbers
- Punctuation
- Stopwords

Stemming is applied to reduce words to their base form.

### Data Visualization
A WordCloud is generated to visualize the most frequent words in the text data.

### Model Training
1. **Vectorization**: The `CountVectorizer` converts text data into a sparse matrix of token counts.
2. **Train-Test Split**: Data is split into training and testing sets using an 80-20 ratio.
3. **Naive Bayes Classifier**: A Bernoulli Naive Bayes model is trained on the data.

### Real-Time Prediction
The trained model predicts stress levels based on user input.

## Usage

1. **Run the Script**
   Execute the script to preprocess the data, train the model, and visualize the WordCloud.

2. **User Input**
   Provide text input to the model for stress classification. Example:

   ```
   Enter a Text: I feel overwhelmed with work.
   Output: ['Stress']
   ```

## Results
The model can accurately classify whether a given text reflects stress or not.

## Contributions
Feel free to contribute to this project by improving the preprocessing steps or trying out different classifiers.

## License
This project is licensed under the MIT License.

