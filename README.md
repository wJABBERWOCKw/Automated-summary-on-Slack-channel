# Automated-summary-on-Slack-channel
Automated Periodic Data summary sent to slack channels  using Python

Dataset- Covid 19 state level data 
which contains
date      datetime64[ns]
state             object
fips               int64
cases              int64
deaths             int64
dtype: object

Data engineering part 
To generate a message with top 3 states with high death percentage on monthly basis 

we first make a column named month in the data set ,then it is grouped by month and country 

for calculating the percentage  we store the deaths /total cases value in separate column named month data

then it is sorted in ascending order and  stored in Monthly_analysis={} for different months march april may june 


SLACK 

To report the trend analysis on slack channel  we must have slack api token and channel id 

by iterating in monthly_analysis messages can be sent messages to the specified channel also after a specific time 


LIBRARIES USED:-

import slack_sdk


import pandas as pd

import datetime

from slack_sdk import WebClient

import time

