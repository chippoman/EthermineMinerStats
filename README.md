# FlexpoolMinerStats
Stats monitoring, recording and charting for Flexpool Miners
By default, stats are saved to Google Sheets once every 5 minutes and when the script is first run

To start monitoring Flexpool stats, run the FlexpoolMinerStats.py file
Libraries required:
* flexpoolapi
* pygsheets
* cryptocompare
* time
* datetime

## Steps
1. Copy this Google sheet to your own Google Drive
https://docs.google.com/spreadsheets/d/1_Hyl4bFd4K2xdYm2YQf3VLd5xkLQiSOeGIJvJWyukyw/edit?usp=sharing

1. Go to the first sheet and copy the URL to your code

1. Copy and insert your Flexpool Miner address to your code

1. Follow the instructions here to receive a client_secret.json file (this is the trickest part)
https://pygsheets.readthedocs.io/en/stable/authorization.html

1. Running the script the first time, an authorization needs to be performed through Google following the link in the console

1. *Go to your Google Sheet to monitor stats*
  * Time
  * ETH Balance
  * ETH-USD Exchange Rate
  * USD Balance
  * 5 min USD change
  * 24 hour rolling difference
  * ETH 5 min change (typically block reward or payout)


### Known Bugs
* Rolling 24h difference does not calculate correctly across payout periods
* Only works for 5 minute intervals, cell references need to be changed if shorter / longer intervals are used
* Update intervals less than 1 minute or >59 minutes not tested
