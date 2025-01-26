# News Categorization using RNN

## Problem Statement
The British Broadcasting Corporation (BBC) aims to automatically categorize news articles into predefined categories. This will enhance user experience by enabling accurate news recommendations based on their preferences.

## Dataset
A dataset consisting of 2225 news articles and their corresponding categories is used for this project.

### Attribute Information:
- `filename`: Name of the file containing the news article.
- `title`: Headline of the news.
- `content`: Main content of the news article.
- `category`: Target variable specifying the type of news.

## Approach
We utilize a Recurrent Neural Network (RNN) with SimpleRNN layers to perform text classification on the news articles based on their titles.

## Data Preprocessing
1. **Cleaning the Data**:
   - Convert text to lowercase.
   - Remove stop words and punctuations.
   - Replace periods (`.`) with `.` followed by a space.
   - Tokenize and join back the cleaned text.

2. **Visualization**:
   - Analyzed the category distribution using bar plots.

3. **Feature Extraction**:
   - Tokenized and padded the text sequences to ensure uniform length.

## Model Architecture
- **Embedding Layer**: Converts words into dense vector representations.
- **SimpleRNN Layer**: Extracts sequential information from the text data.
- **Dense Layer**: Fully connected layer with `softmax` activation for multi-class classification.

### Hyperparameters
- Latent Dimension: 50
- Embedding Dimension: 100
- Batch Size: 64
- Epochs: 10
- Optimizer: Adam
- Loss Function: Categorical Crossentropy

## Training
The dataset is split into 80% training and 20% testing sets. The model is trained with early stopping and tensorboard callbacks for monitoring validation accuracy.

### Results
- **Vocabulary Size**: 1807 unique tokens.
- **Maximum Sequence Length**: Based on the longest title in the dataset.
- **Accuracy**: Achieved an accuracy of `XX%` on the test set.

### Evaluation
- Confusion Matrix: Generated to visualize the classification results.

## Visualization
- Heatmap of the Confusion Matrix:
  - Visualizes the model’s predictions against actual categories.

## Repository Structure
```
├── data
│   ├── bbc-news-data.csv
├── models
│   ├── news_categorization_model.h5
├── src
│   ├── preprocess.py
│   ├── train.py
│   ├── evaluate.py
├── README.md
```

## Future Work
- Experiment with advanced architectures like LSTM, GRU, or transformers.
- Leverage article `content` for more context.
- Implement multilingual support for broader applicability.

---

For more details, refer to the [GitHub Repository]((https://github.com/Aditya2600/News-Categorization-in-BBC)).
