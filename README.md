# lead-news

## Installation for Windows/Powershell (performed from VSCode)

### This was a good sample Django web project, first one I got to actually work from Github
### This was well documented, it just needed a few tweaks to get it to work from Windows/Powershell/VSCode

```shell
git clone https://github.com/Gowtham1729/lead-news
cd lead-news
python -m pip install virtualenv
python -m venv ./lead_news_venv
.\lead_news_venv\Scripts\activate
pip install -r requirements.txt
```

```shell
# Check django installation
python -m django --version
# do db migrate
python manage.py migrate
# Cannot set the api key to empty environmental variable in Powershell (Linux version from original branch does this)
# Must go to https://newsapi.org to create a free API key, return and put it in your NEWS_API_KEY
export NEWS_API_KEY = "<your_free_api_Key>"
# fetch the news of preferred topic (set the topic with --topic tag)
python manage.py populate_news --topic japan
python manage.py runserver
```

```shell
# create superuser
py manage.py createsuperuser
```


- Home - http://127.0.0.1:8000/
- Latest News (Same as Home) - http://127.0.0.1:8000/news/
- Admin Panel - http://127.0.0.1:8000/admin/
- News API endpoints - http://127.0.0.1:8000/api/news

*Note:* Change the port number if the site is running on a different port

## Demo
![lead_news](https://user-images.githubusercontent.com/25081151/219856766-23a9d1ac-b3fa-496a-8be0-063be8d787e0.gif)
