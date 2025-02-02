Summarization Model Evaluation Using TOPSIS

Introduction

This project focuses on evaluating various text summarization models using the TOPSIS (Technique for Order Preference by Similarity to Ideal Solution) method. The goal is to assess the performance of these models based on key metrics—Compression, Readability, Similarity, and Inference Time—to determine which models produce the most efficient and accurate summaries. The results are ranked according to these metrics and visualized through informative plots for easy comparison.

Project Overview

The project compares four advanced text summarization models to evaluate their ability to produce concise summaries while retaining critical information. The models analyzed include:

1. BART (Bidirectional and Auto-Regressive Transformers)

BART is a powerful sequence-to-sequence model optimized for abstractive summarization. It employs a transformer-based architecture to generate coherent, human-like summaries from extensive documents.

2. T5 (Text-to-Text Transfer Transformer)

T5 frames all NLP tasks, including summarization, as text-to-text problems. This versatile transformer model can generate diverse outputs suited to various summarization tasks.

3. Pegasus (Pretrained Text-to-Text Transformer)

Pegasus is fine-tuned specifically for abstractive summarization. Its large-scale pretraining enhances its capability to produce concise, informative summaries, even from complex texts.

4. LED (Long-Document Encoder-Decoder)

LED is designed to handle long documents efficiently. Its modified transformer architecture allows it to process lengthy sequences without truncation, making it ideal for summarizing detailed reports and articles.

Evaluation Metrics

To ensure comprehensive evaluation, the models are assessed using the following metrics:

Compression: Measures the reduction in text length, calculated as the ratio of the summary length to the original text. A lower ratio indicates better compression.

Readability: Assessed using the Flesch Reading Ease score, which evaluates text simplicity based on sentence length and word complexity. Higher scores indicate easier readability.

Similarity: Determined using cosine similarity to compare the generated summary with a reference summary, assessing content accuracy. Higher scores signify greater similarity.

Inference Time: Measures the time taken by each model to generate summaries. Faster inference times are preferable for real-time applications.

System Requirements

Before running the project, ensure the following Python packages are installed:

pip install pandas numpy matplotlib seaborn transformers sentence-transformers textstat scikit-learn

Script Overview

1. Data Preparation:

A lengthy text (e.g., Industrial Revolution summary) and a reference summary are used for evaluation.

2. Model Setup:

Summarization models (BART, T5, Pegasus, LED) are loaded using the Hugging Face Transformers library.

3. Metrics Calculation:

Compression: Ratio of summary length to original text.

Readability: Calculated using the textstat library.

Similarity: Computed using sentence-transformers.

Inference Time: Measured for each model.

4. TOPSIS Evaluation:

The TOPSIS method ranks models based on their metric scores. The weights and impacts are defined as:

Compression: Positive impact (shorter summaries are better).

Readability: Positive impact (higher readability is better).

Similarity: Positive impact (higher similarity is better).

Inference Time: Negative impact (faster inference is better).

5. Visualization:

The results are visualized using various plots:

Bar Plot: Comparing model performance across all metrics.

TOPSIS Score Comparison: Bar plot displaying TOPSIS scores.

Box Plot: Showing the distribution of model ranks.

Heatmap: Visualizing model performance across different metrics.

Usage

To evaluate the models and generate visualizations, run the following command:

python analysis.py

Output Includes:

TOPSIS Results: Ranked models based on their scores.

Visualizations: Bar plots, heatmaps, and box plots for detailed analysis.

Example Output

TOPSIS Results: Screenshot of ranked models.

Bar Plots: Comparing models for Compression, Readability, Similarity, and Inference Time.

TOPSIS Score Comparison: Bar plots showcasing model scores.

Heatmap: Visualization of performance across metrics.

Conclusion

This project provides a structured approach to comparing and ranking text summarization models using the TOPSIS method. The comprehensive evaluation metrics and detailed visualizations support informed decision-making when selecting a summarization model, tailored to specific needs like processing speed or summary quality.
