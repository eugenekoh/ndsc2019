# National Data Science Challenge 2019 - Beginner's Category

This is my first Kaggle Competition. My team joined the beginner's category and the task was Product Category Classification using image and title. Performance was evaluated based on the accuracy of the classification results. Our solution achieved an accuracy of `0.76360` on the private leaderboard and we were ranked `25th out of 360 submisions`.

Kaggle NDSC : https://www.kaggle.com/c/ndsc-beginner

## Solution

- **Data Preprocessing**
  - We tried preprocessing the noisy data by cleaning out numbers, special characters, translating words and correcting errors. However, there were negligible improvements in accuracy
  - A significant portion of the data was mislabelled and we relabeled as much as we could.
- **Model** 
  - Results on images were disheartening , approximately 20% lower in accuracy compared to text classification. So we focused our attention on text.
  - We monitored training with a weighted F1 score as there were large class imbalances.
  - Trained text classifer using FastAI with the two architectures provided - AWD_LSTM and Transformer
- **Model Stacking**
  - We feed our predictions into a logistic regression for our ensemble
