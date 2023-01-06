# Text-Summarization-Multi-News

Multi-News, consists of news articles and human-written summaries of these articles from the site newser.com. Each summary is professionally written by editors and includes links to the original articles cited.

There are two features:

    document: text of news articles seperated by special token "|||||".
    summary: news summary.

The BART model for text summarization was fit and trained for 10 epochs.
The model predicts a new summary given an article.

# Evaluation Metric
The Rouge metric was used for evaluation:

ROUGE-N measures the number of matching ‘n-grams’ between our model-generated text and a ‘reference’. <br />

An n-gram is simply a grouping of tokens/words. A unigram (1-gram) would consist of a single word. A bigram (2-gram) consists of two consecutive words:<br />

For ROUGE-1 we would be measuring the match-rate of unigrams between our model output and reference. <br />
ROUGE-2 and ROUGE-3 would use bigrams and trigrams respectively. <br />
ROUGE-L measures the longest common subsequence (LCS) between our model output and reference. <br />

RougeLsum :Newlines in the text are interpreted as sentence boundaries, and the LCS is computed between each pair of reference and candidate sentences, This is called rougeLsum. <br />

| Model | Epochs | ROUGUE | F1 Score(Weighted) |
| ----- | ------ | -------- | ------------------ |
|BART | 6 | 38 |0.84 |
|DistilBART | 6 | 42 |0.86|

The following research paper has been used for fine tuning the optimizers: [On Empirical Comparisons of Optimizers for Deep Learning](https://arxiv.org/pdf/1910.05446.pdf)

Optimizer | Learning Rate $\gamma$ |   Momentum $\eta$ | Alpha $\alpha$ | Beta1 $\beta_1$ | Beta2 $\beta_2$ | Epsilon $\epsilon$ |
| ---     | ---                    | ---               | ---            | ---             | ---             | ---                |
AdamW     | 5e-5                   | 0.01              | 0.9            | 0.9             | 0.999           | 1e-5               |
RMSprop   | 0.01                   | 0.01              | 0.99           | -               | -               |  -                 |
NAG       | 5e-5 |                 | -                 | -              | -               |-                | -                  |   
SGD(Momentum)| 5e-5                | 0.001             | -              |  -              |-                | -                  |
SGD          | 0.01 |              |  -                | -              | -               |-               | -                   |


    
**Comparing the Training loss of all optimizers**
<br>
<img src = "1.train_loss_all.png">

**Comparing the Test loss of all optimizers**
<br>
<img src = "1.test_loss_all.png">

**Comparing the Validation loss of all optimizers**
<br>
<img src = "1.val_loss_all.png">

The rate of convergence of the Adam optimizer is the fastest.

We can conclude the order of convergence of the optimizers:
AdamW > RMSprop > NAG > SGD (Momentum) > SGD




