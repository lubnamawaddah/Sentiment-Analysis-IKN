# Sentiment Analysis IKN

This project focuses on performing sentiment analysis on YouTube comments related to the IKN (Ibu Kota Nusantara), the New National Capital City project in Indonesia. The goal is to classify comments into three categories: **positive**, **negative**, and **neutral**. The project involves data scraping, preprocessing, modeling, and evaluation using three different machine learning models.

## Project Overview
1. **Data Collection**

   Comments were scraped from 6 YouTube videos discussing IKN, resulting in a dataset of approximately 30,000 entries.
   
2. **Data Preprocessing**

   Comments were cleaned and preprocessed through the following steps:
   - **Text Cleaning:**
     Removed special characters, emojis, and unnecessary symbols.
     Normalized repeated characters (e.g., "sooo goood" to "so good").
   - **Case Folding:**
     Converted all text to lowercase to ensure consistency.
   - **Slang Word Normalization:**
     Replaced informal or slang words with their standard equivalents (e.g., "yg" to "yang").
   - **Tokenization:**
     Split the text into individual tokens (words) for further processing.
   - **Stopword Removal:**
     Removed common stopwords (e.g., "dan", "yang", "di") to focus on meaningful words.
   - **Final Text Preparation:**
     Combined the cleaned tokens back into sentences for analysis.

3. **Data Labeling**

   Classified the comments into three sentiment categories: positive, negative, and neutral.
   
4. **Exploratory Data Analysis (EDA)**

   Visualizations were created to analyze the distribution of sentiments and trends in the dataset.
   
      ![dist](https://github.com/user-attachments/assets/43a0f727-a926-4fdf-b460-74a6fb8909f2)

      ![freq-words](https://github.com/user-attachments/assets/dddcea6c-d4cd-4231-a895-68f9630cc53a)

      ![word-cloud](https://github.com/user-attachments/assets/f39dc37a-bdff-4a5a-8b93-80264f16dd34)

6. **Modeling**

   Three models were trained and evaluated:  
   - **Logistic Regression (LR)** with TF-IDF feature extraction and 70:30 data split.
   - **Long Short-Term Memory (LSTM)** with an 80:20 data split.  
   - **Gated Recurrent Unit (GRU)** with an 80:20 data split.  

7. **Model Evaluation Results**

    | Model                 | Accuracy Train | Accuracy Test |
    |-----------------------|----------------|---------------|
    | Logistic Regression   | 89.59%         | 83.93%        |
    | LSTM                 | 91.83%         | 87.86%        |
    | GRU                  | 92.68%         | 87.98%        |

8. **Prediction**

   The trained models were used to predict sentiments on new, unseen text data.

## Conclusion
This project demonstrates the effectiveness of machine learning and deep learning models for sentiment analysis tasks. While Logistic Regression provided a solid baseline, LSTM and GRU models showed superior performance, highlighting the potential of deep learning for text classification. Further optimization of the LSTM and GRU models could lead to even better results.
