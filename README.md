# AO2020

This repository contains code and data to generate predictions for the 2020 Australian Open. The main code sources are in a-priori-final.ipynb and ex-post.ipynb. 

Here are the results for a few of my ML models and some benchmark models:

|        Model        | Logloss  |   AUC    | Accuracy |
|:-------------------:|----------|---------:|----------|
| a-priori            | 0.529107 | 0.800347 | 0.712598 |
| a-priori-corrected  | 0.522674 | 0.807664 | 0.720472 |
| ex-post             | 0.515281 | 0.825118 | 0.763780 |
| logit-rank-only     | 0.596729 | 0.795449 | 0.720472 |
| indicator-rank-only | 9.654653 | 0.720486 | 0.720472 |

Benchmarks (logit-rank-only and indicator-rank-only) perform surprisingly well in terms of accuracy. a-priori and a-priori-corrected are somewhat medicore. ex-post is superior based on all metrics. Note that for reference, bookmakers got 76.1% of their predictions correct at the 2014 US Open so we're getting comparable performance.

I presented on this at the Learn Data Science Meetup, the video can be found here: https://www.youtube.com/watch?v=XGHQ-s-z0-c&ab_channel=LearnDataScience

I also wrote a Medium article on this which you can read here: https://medium.com/@hxyue1/australian-open-2020-predicting-atp-match-outcomes-7f5fbba62122

This work is an extension of Betfair's 2019 AO Datathon to the 2020. My code isn't original work but a modification of Qile Tan's notebook which you can find here https://github.com/betfair-datascientists/aus-open-datathon/blob/master/python-machine-learning-walkthrough.ipynb. The ATP match level data is obtained from Skoval's Deuce package which scrapes data from Jeff Sackman's repo.
Show them some love: https://github.com/skoval/deuce, https://github.com/JeffSackmann/tennis_atp.

Disclaimer: I'm not sponsored by Betfair, I don't endorse gambling, but if you do choose to gamble based on my predictions, I'm not responsible for any gains or losses you may make, you are.
