# Finding Polarised Communities and Tracking Information Diffusion on Twitter: A Network Approach on the Irish Abortion Referendum
This repository contains the data files used in the analysis for the paper Finding Polarised Communities and Tracking Information Diffusion on Twitter: A Network Approach on the Irish Abortion Referendum. The paper is published in the [Royal Society Open Science](https://royalsocietypublishing.org/doi/full/10.1098/rsos.240454).

## File description
The file `RT8_mentions_anonymised.csv` contains every mention in the full dataset.

The file `RT8_communities_anonymised.csv` contains the community membership of users in the mutual mentions network.

The file `RT8_cascade_anonymised.csv` contains unique IDs to identify every same text in the full dataset.

The file `RT8_tweet_ID.csv` contains every tweet ID gathered for the study. This allows one to retrieve the original tweets using the Twitter API.

## File structure
The file `RT8_mentions_anonymised.csv` contains three columns:
- `from`: the user (pseudo-anonymised) who sends the tweet.
- `to`: the user (pseudo-anonymised) who receives (is mentioned in) the tweet.
- `sentiment`: the sentiment score of the text in the tweet obtained with AFINN<sup>[1]</sup>.

The file `RT8_communities_anonymised.csv` contains two columns:
- `user`: a user (pseudo-anonymised) in the mutual mentions network, as described in the [paper](https://arxiv.org/abs/2311.09196). The user IDs here match the ones in `RT8_mentions_anonymised.csv`.
- `membership`: the user's community membership obtained with the weighted Louvain<sup>[2]</sup> algorithm.

The file `RT8_cascade_anonymised.csv` contains three columns:
- `user`: the user (pseudo-anonymised) that posts the tweet. The user IDs here match the ones in `RT8_mentions_anonymised.csv`.
- `created_at`: the date and time when the tweet was posted.
- `retweet_id`: the ID of the text (equal texts contain same ID).

The file `RT8_tweet_ID.csv` contains a single column with the tweet IDs gathered for the study, which allows for the original tweets to be gathered using the Twitter API.

## Reference
[1] Nielsen FÅ. A new ANEW: Evaluation of a word list for sentiment analysis in microblogs. arXiv preprint arXiv:11032903. 2011.

[2] Blondel VD, Guillaume JL, Lambiotte R, Lefebvre E. Fast unfolding of communities in large
networks. Journal of statistical mechanics: theory and experiment. 2008;2008(10):P10008
