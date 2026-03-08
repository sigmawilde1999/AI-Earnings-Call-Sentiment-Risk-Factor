# AI Earnings Call Sentiment Risk Factor Construction

An NLP-Based Framework for Extracting Text-Derived Risk Signals from Earnings Call Transcripts.

---

## Project Overview

This project develops a quantitative framework for constructing text-based risk factors from corporate earnings call transcripts using financial-domain NLP models.

Earnings calls contain forward-looking qualitative information that is not fully reflected in traditional financial metrics. By applying FinBERT to managerial responses in earnings call Q&A sessions, this project extracts structured sentiment signals and transforms them into interpretable risk indicators.

The objective is not merely sentiment classification, but the construction of economically meaningful risk factors that may complement traditional market-based measures.

---

## Dataset

- Source: META Earnings Call Q&A Dataset (Kaggle)
- Frequency: Quarterly
- Focus: Executive responses (management tone)

The analysis focuses on Q&A sections to better capture spontaneous managerial tone and risk communication.

---

## Methodology

### 1. Text Preprocessing
- Extract executive answers from structured transcript data
- Clean and normalize text inputs

### 2. Financial Sentiment Modeling
- Model: ProsusAI/FinBERT
- Classification: Positive / Neutral / Negative
- Inference performed at answer-level granularity

### 3. Risk Factor Construction

From sentence-level predictions, the following risk indicators are constructed:

- Average Sentiment Score  
- Downside Sentiment Ratio  
- Sentiment Dispersion  
- Sentiment Shock (Quarter-over-Quarter change)

These metrics aim to capture managerial tone dynamics and communication risk.

---

## Key Findings

- Managerial tone is generally positive but exhibits meaningful temporal variation.
- Downside spikes and dispersion increases coincide with periods of elevated uncertainty.
- Text-derived indicators provide complementary qualitative risk information.

---

## Limitations

- Single-firm analysis (META) limits cross-sectional generalizability.
- Predictive power against market returns or volatility is not formally tested.
- Earnings call tone may reflect strategic communication bias.

---

## Future Extensions

- Multi-firm cross-sectional factor construction
- Integration with market return and volatility data
- Event-study validation
- Incorporation of advanced LLM-based contextual modeling

---

## Technical Stack

- Python
- Transformers (HuggingFace)
- FinBERT
- PyTorch
- Pandas / NumPy / Matplotlib

---

## Author

Sigma Wilde  
MSc Financial Engineering  
Focused on Quant Risk & Text-Based Risk Modeling
