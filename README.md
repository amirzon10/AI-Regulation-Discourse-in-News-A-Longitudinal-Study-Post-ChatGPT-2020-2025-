# AI Regulation Discourse in News: A Longitudinal Study Post-ChatGPT (2020-2025)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)

## 📖 Overview

This repository contains a comprehensive longitudinal study analyzing AI regulation discourse across ideologically diverse U.S. news outlets from 2020-2025, with a specific focus on shifts following the release of ChatGPT. Using advanced Natural Language Processing (NLP) techniques, this research traces how media framing, sentiment, and stakeholder narratives evolve over time, revealing how media ideology shapes public understanding of AI policy.

## 🎯 Research Objectives

- Analyze temporal shifts in AI regulation discourse pre and post-ChatGPT release
- Compare framing differences across ideologically diverse news outlets
- Extract and analyze stakeholder narratives through Named Entity Recognition (NER)
- Measure sentiment trends toward AI regulation across different media sources
- Investigate the relationship between political orientation and AI policy framing

## 🗂️ Repository Structure

```
.
├── Data_engineering/
│   ├── language_translation.ipynb       # Multilingual text processing and translation
│   ├── political_orientation.ipynb      # Media outlet political classification
│   └── translation_orientation_merging.ipynb  # Data integration pipeline
│
├── NER_and_sentiment_analysis/
│   ├── NER.ipynb                        # Named Entity Recognition analysis
│   └── sentiment_analysis.ipynb         # Sentiment analysis pipeline
│
├── data/
│   └── [Dataset files - see Data section]
│
├── LICENSE                               # MIT License
└── README.md                             # This file
```

## 📊 Data Processing Pipeline

### 1. **Data Engineering**

#### Language Translation
- **Purpose**: Process MediaCloud dataset (2020-2025) by translating non-English article titles to English
- **Features**:
  - Chunked processing for large-scale datasets (configurable chunks, default: 1000 rows)
  - Utilizes Google Translator API for robust multilingual translation
  - Preserves original English titles while expanding dataset coverage

#### Political Orientation Classification
- **Purpose**: Classify news outlets by political ideology
- **Method**: Data-driven approach to map media sources to political spectrum
- **Output**: Enables comparative analysis across ideological boundaries

#### Data Integration
- **Purpose**: Merge translated content with political orientation metadata
- **Output**: Unified dataset ready for downstream NLP analysis

### 2. **NLP Analysis**

#### Named Entity Recognition (NER)
- **Purpose**: Extract and analyze key stakeholders in AI regulation discourse
- **Entities Tracked**:
  - Organizations (tech companies, regulatory bodies, advocacy groups)
  - Political figures and policymakers
  - Institutions and government agencies
  - Geographic locations
- **Applications**: Stakeholder network analysis, influence mapping

#### Sentiment Analysis
- **Purpose**: Quantify emotional tone and attitude toward AI regulation
- **Method**: 
  - VADER lexicon-based sentiment classification
  - Addresses challenge of unlabeled training data
  - Feature engineering using TF-IDF and Truncated SVD (LSA)
- **Output**: Sentiment scores (positive, negative, neutral) across time and outlet type

## 🛠️ Technologies & Tools

### Core Libraries
- **Data Processing**: `pandas`, `numpy`
- **NLP**: `vaderSentiment`, `spaCy`, `NLTK`
- **Machine Learning**: `scikit-learn` (TF-IDF, TruncatedSVD)
- **Translation**: `deep_translator` (GoogleTranslator)
- **Visualization**: `matplotlib`, `seaborn`

### Environment
- **Language**: Python 3.8+
- **Platform**: Jupyter Notebook
- **Data Source**: MediaCloud (2020-2025)

## 🚀 Getting Started

### Prerequisites

```bash
pip install pandas numpy matplotlib seaborn
pip install vaderSentiment spacy scikit-learn
pip install deep-translator
python -m spacy download en_core_web_sm
```

### Usage

1. **Clone the repository**:
   ```bash
   git clone https://github.com/amirzon10/AI-Regulation-Discourse-in-News-A-Longitudinal-Study-Post-ChatGPT-2020-2025-.git
   cd AI-Regulation-Discourse-in-News-A-Longitudinal-Study-Post-ChatGPT-2020-2025-
   ```

2. **Data Engineering Pipeline**:
   - Run `language_translation.ipynb` to process and translate raw data
   - Run `political_orientation.ipynb` to classify media outlets
   - Run `translation_orientation_merging.ipynb` to integrate datasets

3. **NLP Analysis**:
   - Run `NER.ipynb` for entity extraction and stakeholder analysis
   - Run `sentiment_analysis.ipynb` for sentiment classification

## 📈 Key Features

### Longitudinal Analysis
- **Time Range**: 2020-2025 (5-year span)
- **Key Milestone**: ChatGPT release (November 2022) as temporal pivot point
- **Temporal Granularity**: Article-level timestamps for precise trend analysis

### Cross-Ideological Comparison
- Analysis across left-leaning, center, and right-leaning news sources
- Comparative framing analysis
- Ideology-specific sentiment patterns

### Robust NLP Pipeline
- Lexicon-based sentiment analysis (VADER)
- Feature extraction with dimensionality reduction (TF-IDF + LSA)
- Entity-centric discourse analysis
- Multilingual content processing

## 🔍 Research Insights

This analysis reveals:
- How AI regulation discourse intensified post-ChatGPT
- Ideological differences in framing AI policy debates
- Evolution of stakeholder prominence in media coverage
- Sentiment shifts reflecting changing public perceptions
- Media's role in shaping AI governance narratives

## 📝 Citation

If you use this work in your research, please cite:

```bibtex
@misc{ai_regulation_discourse_2025,
  author = {Amir Freer and Contributors},
  title = {AI Regulation Discourse in News: A Longitudinal Study Post-ChatGPT (2020-2025)},
  year = {2025},
  publisher = {GitHub},
  url = {https://github.com/amirzon10/AI-Regulation-Discourse-in-News-A-Longitudinal-Study-Post-ChatGPT-2020-2025-}
}
```

## 👥 Contributors

This project is a collaborative research effort:

- [**Vrynsiaa**](https://github.com/Vrynsiaa) - Vrynsia
- [**Johnifec**](https://github.com/Johnifec) - Johnpaul  
- [**amirzon10**](https://github.com/amirzon10) - Amir Freer
- [**DataScience154**](https://github.com/DataScience154)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

## 📧 Contact

For questions or collaboration opportunities, please reach out through GitHub issues or contact the repository owner.

## 🙏 Acknowledgments

- MediaCloud for providing the news article dataset
- The open-source NLP community for invaluable tools and libraries
- All contributors who made this research possible

---

**Note**: This is an academic research project. Data analysis findings and interpretations are subject to peer review and ongoing refinement.
