# Finding Polarised Communities and Tracking Information Diffusion on Twitter: A Network Approach on the Irish Abortion Referendum
This repository contains the files used in the analysis for the paper Finding Polarised Communities and Tracking Information Diffusion on Twitter: A Network Approach on the Irish Abortion Referendum. An arXiv preprint can be found [here](https://arxiv.org/abs/2311.09196).

## File description
The file `RT8_mentions_anonymised.csv` contains every mention in the full dataset.

The file `RT8_cascade_anonymised.csv` contains unique IDs to identify every same text in the full dataset.

The file `RT8_tweet_ID.csv` contains every tweet ID gathered for the study. This allows one to retrieve the original tweets using the Twitter API.

## File structure
The file `RT8_mentions_anonymised.csv` contains three columns:
- `from`: the user (anonymised) who sends the tweet.
- `to`: the user (anonymised) who receives (is mentioned in) the tweet.
- `sentiment`: the sentiment score of the text in the tweet obtained with AFINN<sup>[1]</sup>.

The file `RT8_cascade_anonymised.csv` contains three columns:
- `user`: the user (anonymised) that posts the tweet. The user IDs here match the ones in `RT8_mentions_anonymised.csv`.
- `created_at`: the date and time when the tweet was posted.
- `retweet_id`: the ID of the text (equal texts contain same ID).

The file `RT8_tweet_ID.csv` contains a single column with the tweet IDs gathered for the study, which allows for the original tweets to be gathered using the Twitter API.

## Reference
<sup>[1]</sup> Nielsen FÅ. A new ANEW: Evaluation of a word list for sentiment analysis in microblogs. arXiv preprint arXiv:11032903. 2011.
