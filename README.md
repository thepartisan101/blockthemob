# BlockTheMob
A tool to identify and list the perennialy outraged accounts in social media, and automatically block them from seeing the user posts, preventing future damage.

## Motivation
There is a minority of social media users that, not willing to have a civilized conversation, prefer to interpret others statements in the worst light possible, not giving the benefit of the doubt. They proceed to post hateful, fallacious or otherwise overtly negative content, call out other social media users to join in on the "virtual beating", sometimes reporting the original post to social media moderators to silence the author. Whatever their reasons and motivations, this "digital world" problem has become a real-world one, where these reactions have brought phisical harrasment, death threats, jobs lost, etc.

Now, when social media platforms have tried to avoid these situations, it has resulted in silencing potentially mob-inciting speech, instead of blocking these mobs from happening.

This project is intended as a tool to ease the user social media life, present and future, by searching and listing for usernames belonging to accounts that seem to find outrage and mobcreation as a sport. You don't need to be an influencer to use it, when this project is mature, you should be able to run this program and block the uncivilized even if you don't know them, or have never interacted with them at all. This way, when your social following will grow, or if you post a tweet that happens to go viral, you'll have a higher chance of avoiding the ire of the keyboard warrior. Peaceful replies, peaceful life.

## Development
This project will be based on Python (most of the best NLP and data science libraries are made for it)

## Roadmap
#### 1. Data gathering
1. [] List Twitter controversies/fights (w/ celebrities, authors...)
    1. [List of banned people and reasons](https://en.wikipedia.org/wiki/Twitter_suspensions)
2. [] List of all SJW twitter fights?
3. [] List of most followed accounts by SJWs?
    1. [] Is there a site tracking them?
    2. [] List their followers
    3. [] List most extreme SJW influencers, black-list followers
4. [] List of #Hashtags used by SJWs, Saudi trolls,  foreign govs agencies, or accounts, find users and add to list
    1. [Explore Twitter Trending Topics](https://www.trendsmap.com/)
    2. [Example](https://twitter.com/hashtag/TransIsBeautiful?src=hash)
    3. Create a script that looks for new hashtags coming from specific countries(dictatorships) or blacklisted accounts by account/event monitoring, tracks who is sharing them, and adds them to list.
5. For each controversial Tweet obtain URL
6. Use existing twitter scrapers to get original Tweet and replies
    1. [How to scrape Twitter for Historical Tweet Data](https://www.scrapehero.com/how-to-scrape-historical-search-data-from-twitter/)
    2. [Github - TweetScraper](https://github.com/jonbakerfish/TweetScraper)
    3. [Scrape tweets without using the API](http://www.simonlindgren.com/stuff/2017/11/7/scrape-tweets-without-using-the-api)
7. [] Export to JSON/CSV Reply-Content | Reply-author
#### 2. Data processing and NLP -> List creation
 1. [] Original Tweet: Identify topic-idea
 2. [] Replies: Sentiment analysis + topic extraction
 3. [] Create a list from very negative to extremely negative replies (sentimen[-0.5:-1])
 4. [] For tweet in negative tweets:
    1. Is it intended towards the author or the topic?
    2. If it's against the author -> Add account to blocked_list
#### 3. Script to automatically block listed users
   1. Get user Twitter login manually or through API, start broser and login w/ Selenium.
   2. Go through users from list and automatically click on "Block user"
   3. Package script as .exe or a web app?
   4. Run twitter NLP scanning through a P2P network like Seti@home project?
#### 4. Public lists of users by topic?
Perhaps creating lists of blacklisted users by topic? - Useful for users that focus their content around specific industries, or for companies that want to avoid unnecessary backlash (might be a service to sell)


