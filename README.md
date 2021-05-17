# sentiment_analysis

This notebook for web-scraping from Yahoo Finance is inspired by the work under

https://github.com/nicknochnack/Stock-and-Crypto-News-ScrapingSummarizationSentiment 

https://www.youtube.com/watch?v=YbKnsJQKazA 

In the notebook recent articles about Bitcoin are first extracted from Yahoo Finance by using BeautifoulSoup. 
With the help of Hugging Face transformers the articles are summarised. 
Finally on the summaries we run sentiment analysis and we look at the distribution of the sentiment.

The following part of the code

search_url = "https://www.google.com/search?q=yahoo+finance+{}&tbm=nws".format(ticker)

r = requests.get(search_url)

had log-in + cookies problems with Google. A work around by using the pygooglenews library has been implemented.
