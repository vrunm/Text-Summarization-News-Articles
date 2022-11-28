# Text-Summarization-Multi-News

Multi-News, consists of news articles and human-written summaries of these articles from the site newser.com. Each summary is professionally written by editors and includes links to the original articles cited.

There are two features:

    document: text of news articles seperated by special token "|||||".
    summary: news summary.

The BART model for text summarization was fit and trained for 10 epochs.
The Rouge metric was used for evaluation:
| Epoch    | Training Loss | Validation Loss | Rouge1    |   Rouge2 |  Rougel | Rougelsum | Gen Len
| 1        | 2.543800      | 2.369417        | 33.615200 | 12.164400 | 20.592400| 20.607000 | 61.9666000|
| |          |
|     | |        |

| Command | Description |
| --- | --- |
| `git status` | List all *new or modified* files |
| `git diff` | Show file differences that **haven't been** staged |
