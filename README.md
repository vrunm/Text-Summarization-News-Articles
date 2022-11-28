# Text-Summarization-Multi-News

Multi-News, consists of news articles and human-written summaries of these articles from the site newser.com. Each summary is professionally written by editors and includes links to the original articles cited.

There are two features:

    document: text of news articles seperated by special token "|||||".
    summary: news summary.

The BART model for text summarization was fit and trained for 10 epochs.
The Rouge metric was used for evaluation:
<img src = "plots/1.epochs_table.png">

<img src = "plots/2.bart_rouge2.png">

<img src = "plots/3.bart_rougeLsum.png">

<img src = "plots/4.bart_rouge1.png">

<img src = "plots/5.bart_eval_rougeL.png">

