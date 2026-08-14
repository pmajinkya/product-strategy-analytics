# product-strategy-analytics
Python scripts leveraging NLP and Gemini AI for customer feedback analysis and competitive intelligence.

Project 1: AI Customer Feedback Embedding & Semantic Clustering Pipeline
Description: Building upon semantic clustering, this advanced script fully automates the triage of raw customer feedback. After grouping feedback into mathematical clusters using NLP and K-Means, it iterates through each cluster and queries the Gemini AI API to automatically generate a Theme Name, assign a Priority Level (Low, Medium, High, or Critical), and write an Executive Summary for the core user pain point. The script then maps these AI-generated labels back into an interactive Plotly visualization. This workflow demonstrates a powerful method for scaling user research, quickly identifying critical system regressions, and ensuring engineering bandwidth is focused on the highest-impact user problems.

Project 2: Competitive Intelligence & Feature Release Digest
Description: This script automates the process of market research and competitor analysis. It works by scraping raw release notes and changelog data from competitor websites (such as Linear and GitHub). After extracting the web data, the script securely passes the payload to the Google Gemini AI API with a custom prompt to synthesize the information. The output is an executive-level "Monthly Competitive Intelligence & Roadmap Memo," complete with a competitor release matrix, identified market threats, and prioritized counter-strategies. This project highlights the ability to monitor the competitive landscape and rapidly translate market shifts into strategic product recommendations.

Project 3: Customer Feedback Semantic Clustering Pipeline
Description: This project demonstrates how to transform qualitative customer feedback into actionable, quantitative insights using Natural Language Processing (NLP). The Python script uses sentence-transformers to generate vector embeddings from raw user feedback and applies K-Means clustering to group them into distinct semantic categories. Finally, it uses Principal Component Analysis (PCA) to reduce the data dimensions and renders an interactive visual map using Plotly. This tool is highly valuable for visualizing user pain points at a glance and making data-informed decisions for agile backlog prioritization.


INSTRUCTIONS FOR USE

---- Global Prerequisites ----
To run any of these scripts, users will need:
• A Python environment capable of running Jupyter Notebooks (Google Colab is highly recommended for ease of use).
• A free Google Gemini API Key (required for Projects 2 and 3).

Project 1: AI Customer Feedback Embedding & Semantic Clustering
This script combines local machine learning models with the Gemini API to automatically label data.
Steps to use:
• Open the AI_Customer_Feedback_Embedding_&_Semantic_Clustering_Pipeline.ipynb file. 
• Run the first cell to install the necessary libraries (sentence-transformers, scikit-learn, plotly, pandas, and google-genai). 
• In the second cell, locate the feedback_data list and replace the simulated data with your own raw customer feedback. 
• Run the second cell. When prompted, paste your Google Gemini API Key and press Enter. 
• The script will automatically generate vector embeddings, group them mathematically, and iteratively query the gemini-3-flash-preview model to generate a "Theme Name," "Priority Level," and "Executive Summary" for each cluster. 
• Wait a moment for the AI to finish processing; the script will then render an interactive Plotly map where the clusters are color-coded and labeled with the AI-generated themes.  

Project 2: Competitive Intelligence & Feature Release Digest
This script requires an active internet connection to scrape competitor websites and a Gemini API key for synthesis.
Steps to use:
• Open the Competitive_Intelligence_&_Feature_Release_Digest.ipynb file. 
• Run the first cell to install the required libraries, including beautifulsoup4, requests, google-genai, and pandas. 
• In the second cell, locate the competitor_urls dictionary.
• Update the names and URLs to point to the actual changelogs, release notes, or engineering blogs of your specific competitors. 
• Run the second cell. A secure prompt will appear asking you to paste your Google Gemini API Key.  Paste your key and press Enter.
• The script will scrape the specified web pages, pass the raw data to the gemini-3.5-flash model, and print a formatted "Monthly Competitive Intelligence & Roadmap Memo" directly in the output.

Project 3: Customer Feedback Semantic Clustering Pipeline
This script runs locally and does not require an API key.
Steps to use:
• Open the Customer_Feedback_Semantic_Clustering_Pipeline.ipynb file in your Jupyter environment. 
• Run the first cell to install the required dependencies, including sentence-transformers, scikit-learn, plotly, pandas, and google-genai. 
• In the second cell, locate the feedback_data list.
• Replace the simulated sample sentences with your own qualitative customer feedback data (e.g., exported from Zendesk, App Store reviews, or user interviews). 
• Run the second cell to generate vector embeddings using the all-MiniLM-L6-v2 model and group the data using K-Means clustering. 
• Run the final cell to render the interactive visual cluster map using Plotly.
