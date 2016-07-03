# Web Crawler Scrapy of APP Store(Xiaomi)

## Description
We will create a Scrapy project to crawl the content in the Xiaomi Appstore homepage or any other Appstore homepage. Then Save the crawled content in MongoDB. Install Python MongoDB driver and modify pipelines.py to insert crawled data into MongoDB. Crawl more content by following next page links. 
## Plan

### Time
We started this project on 06/04/2016 and have done on 07/02/2017.

### Demo

  - Screenshot
  - GIF
  - Link

### Usage
1. Install Scrapy, MongoDB, Splash and ScrapyJS.(If you already have, skil this step. ）
  - [Scrapy](http://doc.scrapy.org/en/latest/intro/install.html)
  - [MongoDB](https://docs.mongodb.com/master/installation/)
  - [Splash](https://splash.readthedocs.io/en/stable/install.html)
  - [ScrapyJS](https://pypi.python.org/pypi/scrapyjs)
2. Start your Splash and MongoDB server.
  -under catalog /MongoDB/bin:
```bash
    ./mongod
```
  -On the Terminal of docker:
```bash
    docker run -p 8050:8050 scrapinghub/splash
```
3. Clone a copy of the main appstore crawler repo by running:
```bash
    git clone https://github.com/AnkaiLiang/-12WebCralwer.git
```
4. Modify the file -12WebCralwer/appstore_crawler/appstore_crawler/settings.py
Set your Splash server address and the information of MongoDB
In my case, it's :
```python
    SPLASH_URL = 'http://192.168.99.100:8050'
    MONGODB_SERVER = "localhost"
    MONGODB_PORT = 27017
    MONGODB_DB = "Xiaomi"
    MONGODB_COLLECTION = "appdate"
```
5. Go to the catalog /appstore_crawler/, Run the crawler:
    Scrapy crawl xiaomi

### Team
We have 4 people in our team. And we independently complete the entire project coding.
### Acknowledgement
BitTiger

## Resource
- [BitTiger Project: Web Crawler Scrapy](https://www.bittiger.io/microproject/oYDSG6MSFihpiNJ66)
- [Scrapy](http://scrapy.org)
- [MongoDB](https://www.mongodb.org)
- [Splash & ScrapyJS](https://github.com/scrapinghub/scrapy-splash)
- [ScrapyJS & ScrapyJS](https://blog.scrapinghub.com/2015/03/02/handling-javascript-in-scrapy-with-splash/)

## License
See the [LICENSE](LICENSE.md) file for license rights and limitations (MIT).

## Project Information
- category: full stack
- team: 12WebCralwer
- description: a Scrapy project to crawl the content in the Xiaomi Appstore homepage
- stack: mongodb, python


