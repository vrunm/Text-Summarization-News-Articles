# Text-Summarization-Multi-News

Multi-News, consists of news articles and human-written summaries of these articles from the site newser.com. Each summary is professionally written by editors and includes links to the original articles cited.

There are two features:

    document: text of news articles seperated by special token "|||||".
    summary: news summary.

The BART model for text summarization was fit and trained for 10 epochs.
The model predicts a new summary given an article.
The Rouge metric was used for evaluation:

ROUGE-N measures the number of matching ‘n-grams’ between our model-generated text and a ‘reference’. <br />

An n-gram is simply a grouping of tokens/words. A unigram (1-gram) would consist of a single word. A bigram (2-gram) consists of two consecutive words:<br />

For ROUGE-1 we would be measuring the match-rate of unigrams between our model output and reference. <br />
ROUGE-2 and ROUGE-3 would use bigrams and trigrams respectively. <br />
ROUGE-L measures the longest common subsequence (LCS) between our model output and reference. <br />

RougeLsum :Newlines in the text are interpreted as sentence boundaries, and the LCS is computed between each pair of reference and candidate sentences, This is called rougeLsum. <br />





<img src = "1.epochs_table.png">
<img src = "2.bart_eval_rouge1.png">
<img src = "3.bart_rouge2.png">
<img src = "4.bart_eval_rougeL.png">
<img src = "5.bart_rougeLsum.png">
<img src = "6.bart_gen_len.png"

