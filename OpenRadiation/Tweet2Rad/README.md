# Tweet2Rad
Twitter's bot who tweet OpenRadiation data. About this citizen-based not-for-profit project see [OpenRadiation web site](https://www.openradiation.org/en/about-us).

---
## Requirements

Python 3 and modules, see [requirements](requirements.txt) : 

- matplotlib
- json
- requests
- local
- tweepy
- yaml
- datetime

## Setup

You need to have an a valided Twitter app. Add in the file `Tweet2Rad.yml` elements of your Twitter app and OpenRadiation account : api url, api key, userid, tag (like town), number of days for history), with lines:
```
# Twitter API
CONSUMER_KEY: "XXXXXX"
CONSUMER_SECRET: "XXXXXXX"
ACCESS_KEY: "XXXXXXX"
ACCESS_SECRET: "XXXXXXX"

#OpenRadiation API
OR_API: "XXXXXXX"
OR_APIKEY: "XXXXXXX"
OR_API_TYPERESPONSE: "complete"
OR_API_USERID: "XXXXXXX"
OR_API_TAG: "XXXXXXX"
OR_API_MAXNUMBER: "8"
```
## How to run

Tweet2Rad call your own OpenRadiation data (with userid) and post a tweet with the last mesure of the day and a graphical history from the last 8 mesures.

- To launch : `python3 Tweet2Rad.py` (or use crontab it)
- To test : a Jupyter notebook version is awailable.

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/spouyllau/loisir/master?filepath=Tweet2Rad%2FTweet2Rad.ipynb)

