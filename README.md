# ilmbot
A Twitter bot for the twitter account of my podcast ILM FM:

## Website:
http://ILM.FM

## Description:
This is a twitter bot specific for the ILM FM science podcast's twitter account. It has the following functions:
* Parses science news websites searching for science articles and tweets a random article.
* Tweets an annoucement when an episode is published, uses RSS therefore you can keep the script on repeat and will not tweet as long as the RSS has not been updated.

## How to Use:
1. Install Dependecies

`sudo apt update && sudo apt full-upgrade && sudo apt install python3-bs4 python3-lxml python3-twython`

2. Add the Twitter credentials to the script.
3. You can excute the script manually `python3 ilm.py`. A more efficient way is to setup a crons job (times are in UTC):

`crontab -e`

`00 00 * * * python3 ilm.py >> ilm_Log 2>&1`

`32 17 * * * python3 ilm.py >> ilm_Log 2>&1`

`12 18 * * * python3 ilm.py >> ilm_Log 2>&1`

`03 19 * * * python3 ilm.py >> ilm_Log 2>&1`

`08 20 * * * python3 ilm.py >> ilm_Log 2>&1`

## Configuration
Add a new RSS feed to the list called RSSlist on line 22
