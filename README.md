# FAKE_BOT
Telegram bot that detects fake news

## Project Structure:
### folder main_db stores 2 databases:
__confidence.db__ (id of author, his name, number of true and false news from his name)

__mail.db__ (id of user, id of his telegram account)
### folder jupyter_correlation:
 finding correlations in the dataset
### Folder save_train:
 saved trained logistic and linear regression models, and also saved text vectorization training.
### Folder main_datasets: 
 dataset of fake and true news stories
 
### main.ipynb:
writing machine learning model
### bot.py - asynchronous telegram bot written in aiogram. Having the following functions:
*Checking the news* (If available, the author is indicated and added to the authors database (it contains the author's name, the number of false and true news from him))

*Output top 10 authors with the highest level of trust*

*Subscription to the newsletter* (when the model determines that the article is fake, the bot sends it to all users (who subscribed to the newsletter) from the database(it contains telegram id of each user))

***
## How to run the project(windows 10 + windows PowerShell):

In the console: go to the folder where we want to clone the project to
```git clone https://github.com/RedPunk77/FAKE_BOT.git``.

Install all necessary libraries:
```pip install -r requirements.txt```.

Create a config.py file and specify the token of your bot.
```TOKEN="YOUR_TOKEN"```

Run bot.py
```python bot.py```
