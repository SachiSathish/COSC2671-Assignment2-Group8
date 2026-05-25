COSC 2671 — Assignment 2 | Group 8
The Great Exodus: Did Mastodon Become a Real Community After Users Left Twitter/X?

Team Members:
- Bijo Babu Daniel (s4137699)
- Sachin Sathish Krishnan (s4140718) — Team Leader
- Serena Jibu Varghese (s4144470)

================================================================
ORDER OF EXECUTION
================================================================

Run the notebooks in this order:

1. s4140718_PG_Group8_01_DataExtraction_and_Cleaning.ipynb
   - Collects data from Mastodon public API
   - No authentication required
   - Input:  mastodon_data/
   - Output: mastodon_data/
   - Output: mastodon_data_clean/

3. s4140718_PG_Group8_03_InitialInsights_and_NetworkAnalysis.ipynb
   - Exploratory analysis and visualisations
   - Network construction, centrality, community detection, Gephi export
   - Input:  mastodon_data_clean/
   - Output: Charts displayed inline
   - Output: mastodon_data_network/

5. s4140718_PG_Group8_05_NLPAnalysis.ipynb
   - VADER sentiment analysis and LDA topic modelling
   - Input:  mastodon_data_clean/toots_english.csv
   - Output: mastodon_data_nlp/

================================================================
REQUIRED PACKAGES
================================================================

Install all dependencies with:

pip install requests pandas numpy networkx python-louvain
pip install matplotlib pyvis gensim nltk vaderSentiment
pip install scikit-learn wordcloud

For NLTK downloads (run once inside notebook):
import nltk
nltk.download('stopwords')
nltk.download('punkt')

NetworkX version: 2.5 (betweenness workaround applied in notebook 4)

================================================================
CONTENTS OF GITHUB RESPOSITORY
================================================================

  - code/ (All Jupyter Notebook files)
  - README.txt
  - Access_s4140718_PG_Group_08.txt
  - mastodon_data_clean/  (cleaned datasets)
  - gephi_output/ (PNG of instance network)
  - Report_s4140718_PG_Group_08.pdf
  - Worksheet_s4140718_PG_Group_08.pdf

================================================================
RUNNING THE ANALYSIS (Skip Notebook 1)
================================================================
If you want to skip the data extraction step (which will take more than 10 minutes), please refer to the steps below:

The full cleaned dataset is included in the mastodon_data_clean/
folder. This is under 10MB and contains all files needed to run
the analysis directly.

To skip data collection and run the analysis immediately:

1. Start from Notebook 2 (02_s4140718_PG_Group_08.ipynb)
   - Input: mastodon_data_clean/
   - Output: mastodon_data_network/

2. Then run Notebook 3 (03_s4140718_PG_Group_08.ipynb)
   - Input: mastodon_data_clean/toots_english.csv
   - Output: mastodon_data_nlp/

================================================================
NOTES
================================================================

- All data is collected from Mastodon's public REST API
- No private credentials are stored anywhere in this codebase
- The Gephi visualization is stored in the gephi_output folder.