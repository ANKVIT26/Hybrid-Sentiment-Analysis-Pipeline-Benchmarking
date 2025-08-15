# Hybrid-Sentiment-Analysis-Pipeline-Benchmarking
Using the Amazon Fine Food Reviews dataset, Built a Python NLP workflow pairing NLTK/VADER for rapid, rule‑based sentiment scoring with Hugging Face RoBERTa for deeper, context‑aware analysis. Both models ran on identical texts, results were merged for comparison, revealing strong agreement on clear sentiments.
# Tech Stack: Python, Pandas, Matplotlib, NLTK, VADER, Hugging Face Transformers (RoBERTa), PyTorch


Imported NLTK core libraries to prepare for text preprocessing and tokenization.

Used NLTK’s data packages to normalize text (lowercasing, punctuation removal) before sentiment scoring.

Integrated VADER from NLTK for rule‑based sentiment analysis on review texts.

VADER provided quick polarity scores (compound) and classified sentiments as neg, neu, or pos.

Prepared the same dataset subset for transformer‑based analysis to ensure fair model comparison.

Loaded the RoBERTa sentiment model from Hugging Face’s transformers library.

Tokenized and batch‑processed the same reviews using RoBERTa for context‑aware classification.

Extracted RoBERTa’s highest‑probability label (neg, neu, pos) and corresponding confidence score.

Stored both VADER and RoBERTa outputs in a unified Pandas DataFrame for side‑by‑side evaluation.

Generated sample prediction tables to manually inspect differences between the two models.

Produced a bar chart comparing compound scores from VADER and probability‑based scores from RoBERTa.

Computed Agreement Crosstab to quantify where both models agreed or disagreed in classification.

Agreement stats showed high alignment on clear positives and negatives, with some mismatch on neutrals.

For this sample: perfect agreement on strong sentiments, but VADER occasionally labeled borderline neutrals as negative.

Insights highlight VADER’s speed and RoBERTa’s nuance, forming the basis for a hybrid “fast‑then‑deep” pipeline in future runs.

# Final Comparison of both pipelines on same batch text
<img width="1379" height="439" alt="image" src="https://github.com/user-attachments/assets/d1d01687-2419-4dbf-919d-50698fb269a8" />
<img width="860" height="388" alt="image" src="https://github.com/user-attachments/assets/d231ab51-7943-4ad8-a8c2-159308c8b884" />


