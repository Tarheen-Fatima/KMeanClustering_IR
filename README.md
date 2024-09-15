# Web Page Clustering using K-means

# Project Description
This project demonstrates how to scrape text from web pages, preprocess the text data, and use K-means clustering to group similar web pages. The project performs the following:
1. Web scraping using requests and BeautifulSoup.
2. Text preprocessing (tokenization, stopwords removal, lemmatization) using NLTK.
3. Vectorizing text using TF-IDF.
4. Clustering the web pages using K-means.
5. Dimensionality reduction with Truncated SVD for visualization in 2D.
6. Visualization of clusters using Matplotlib.

# Key Features
- Web scraping from URLs to extract textual content.
- Preprocessing of text using NLTK (tokenization, lemmatization, and stopword removal).
- TF-IDF vectorization to convert text into numerical form.
- K-means clustering to group similar web pages into clusters.
- Dimensionality reduction for easy visualization of clusters.
- Interactive plot showing how web pages are grouped by similarity.

# Technology Stack
- Python: Main programming language used.
- Libraries:
  - NLTK: For natural language processing tasks like tokenization and lemmatization.
  - requests: To fetch web pages from the internet.
  - BeautifulSoup: For web scraping and extracting text from HTML.
  - Scikit-learn: For TF-IDF vectorization, K-means clustering, and dimensionality reduction with Truncated SVD.
  - Matplotlib: To visualize clusters in 2D.

# Pre-requisites
Before running this project, ensure that you have Python 3.x installed on your machine along with the required Python libraries.

You can install Python from [here](https://www.python.org/downloads/).

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/KMeanClustering_IR.git
   cd WebPageClustering
   ```

2. Install the required libraries:
   ```bash
   pip install nltk requests beautifulsoup4 scikit-learn matplotlib
   ```

3. Download necessary NLTK resources:
   ```bash
   python -c "import nltk; nltk.download('punkt'); nltk.download('stopwords'); nltk.download('wordnet')"
   ```

# Usage

1. Set URLs to Scrape: 
   Modify the `urls` list in the code with the URLs of the web pages you want to scrape and cluster:
   ```python
   urls = [
       'https://en.wikipedia.org/wiki/Artificial_intelligence',
       'https://en.wikipedia.org/wiki/Machine_learning',
       'https://en.wikipedia.org/wiki/Computer_vision',
       'https://en.wikipedia.org/wiki/Web_scraping'
   ]
   ```

2. Run the Script:
   Execute the script in your terminal or IDE:
   ```bash
   python clustering_web_pages.py
   ```

3. Cluster Visualization: 
   The output will be a 2D scatter plot where each web page is plotted as a point, with colors indicating different clusters.

4. Cluster Labels:
   The script also prints the assigned cluster labels for each web page, so you can see which pages were grouped together.

# Output

# 1. Cluster Visualization
A scatter plot will be generated, showing the 2D representation of the web pages clustered by similarity.

# 2. Cluster Labels for Web Pages
```
Cluster labels for web pages:
Web Page 0: Cluster 1
Web Page 1: Cluster 0
Web Page 2: Cluster 1
Web Page 3: Cluster 2
```

# Customization
- Change the Number of Clusters: You can modify the number of clusters `k` in the K-means algorithm by setting:
   ```python
   k = 3  # or any number of clusters
   ```

- Add More URLs: Add more URLs to the `urls` list to cluster more web pages.

- Text Preprocessing: You can modify the text preprocessing function to suit your needs, such as removing more specific stopwords or using stemming instead of lemmatization.

# Contributing

Contributions are welcome! If you want to contribute:
1. Fork the repository.
2. Create a new feature branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -m 'Added new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
