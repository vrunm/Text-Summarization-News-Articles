# Text-Summarization-Multi-News

Multi-News, consists of news articles and human-written summaries of these articles from the site newser.com. Each summary is professionally written by editors and includes links to the original articles cited.

There are two features:

    document: text of news articles seperated by special token "|||||".
    summary: news summary.

The BART model for text summarization was fit and trained for 10 epochs.
The Rouge metric was used for evaluation:
| Name     | Character |
| ---      | ---       |
| Backtick | `         |
| Pipe     | \|        |
