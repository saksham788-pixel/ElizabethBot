# Elizabeth
<p align="center">
    <a href="https://github.com/MR-SHRLCK/Elizabethbot/commits/master"><img src="https://img.shields.io/github/last-commit/MR-SHRLCK/Elizabethbot/master?label=Last%20Commit&style=flat-square&logo=github&color=F10070" alt="Commit" /></a>
    <a href="https://github.com/MR-SHRLCK/Elizabethbot/stargazers"><img src="https://img.shields.io/github/stars/MR-SHRLCK/Elizabethbot?label=Stars&style=flat-square&logo=github&color=F10070" alt="Stars" /></a>
    <a href="https://github.com/MR-SHRLCK/Elizabethbot/network/members"><img src="https://img.shields.io/github/forks/MR-SHRLCK/Elizabethbot?label=Fork&style=flat-square&logo=github&color=F10070" alt="Fork" /></a>
</p>

![logo](https://telegra.ph/file/0157c7b6cd269654ee987.jpg)
<p align="center">

[ <b> <code> ᴇʟɪᴢᴀʙᴇᴛʜ 2.0 </code> </b> ](https://github.com/Mr-SHRLCK/Elizabeth-2.0)  Tap the banner ⚠️
</p>


# credits
<b>All credits belongs to [dark prince](https://github.com/Mr-Dark-Prince) because it's his work I just take his repo with his permission.. and his efforts all are unforgoted</b>

[![forthebadge made-with-python](http://ForTheBadge.com/images/badges/made-with-python.svg)](https://www.python.org/)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://github.com/p-rinc-e/Elizabeth/graphs/commit-activity)

### Configuration

There are two possible ways of configuring your bot: a config.py file, or ENV variables.

The prefered version is to use a `config.py` file, as it makes it easier to see all your settings grouped together.
This file should be placed in your `Elizabeth` folder, alongside the `__main__.py` file . 
This is where your bot token will be loaded from, as well as your database URI (if you're using a database), and most of 
your other settings.

It is recommended to import sample_config and extend the Config class, as this will ensure your config contains all 
defaults set in the sample_config, hence making it easier to upgrade.

An example `config.py` file could be:
```
from Elizabeth.sample_config import Config


class Development(Config):
    OWNER_ID = 1308628659   # my telegram ID
    OWNER_USERNAME = "Sak_Anya"  # my telegram username
    API_KEY = "1708244564:AAGCdfCHgKVILpcVSf2r2lP-bdaizVh8m30"  # my api key, as provided by the botfather
    SQLALCHEMY_DATABASE_URI = 'postgresql://username:password@localhost:5432/database'  # sample db credentials
    MESSAGE_DUMP = '-1464280498' # some group chat that your bot is a member of
    USE_MESSAGE_DUMP = True
    SUDO_USERS = [1797179225 1521131774 1406657231 1612881302]  # List of id's for users which have sudo access to the bot.
    LOAD = []
    NO_LOAD = ['translation']
    WHITELIST_USERS = []
    BAN_STICKER = [https://telegra.ph/file/49b47668dd9e8ba274cb6.jpg]
```

If you can't have a config.py file (EG on heroku), it is also possible to use environment variables.
The following env variables are supported:
 - `ENV`: Setting this to ANYTHING will enable env variables

 - `TOKEN`: Your bot token, as a string.
 - `OWNER_ID`: An integer of consisting of your owner ID
 - `OWNER_USERNAME`: Your username

 - `DATABASE_URL`: Your database URL
 - `MESSAGE_DUMP`: optional: a chat where your replied saved messages are stored, to stop people deleting their old 
 - `LOAD`: Space separated list of modules you would like to load
 - `NO_LOAD`: Space separated list of modules you would like NOT to load
 - `WEBHOOK`: Setting this to ANYTHING will enable webhooks when in env mode
 messages
 - `URL`: The URL your webhook should connect to (only needed for webhook mode)

 - `SUDO_USERS`: A space separated list of user_ids which should be considered sudo users
 - `SUPPORT_USERS`: A space separated list of user_ids which should be considered support users (can gban/ungban,
 nothing else)
 - `WHITELIST_USERS`: A space separated list of user_ids which should be considered whitelisted - they can't be banned.
 - `DONATION_LINK`: Optional: link where you would like to receive donations.
 - `CERT_PATH`: Path to your webhook certificate
 - `PORT`: Port to use for your webhooks
 - `DEL_CMDS`: Whether to delete commands from users which don't have rights to use that command
 - `STRICT_GBAN`: Enforce gbans across new groups as well as old groups. When a gbanned user talks, he will be banned.
 - `WORKERS`: Number of threads to use. 8 is the recommended (and default) amount, but your experience may vary.
 __Note__ that going crazy with more threads wont necessarily speed up your bot, given the large amount of sql data 
 accesses, and the way python asynchronous calls work.
 - `BAN_STICKER`: Which sticker to use when banning people.
 - `ALLOW_EXCL`: Whether to allow using exclamation marks ! for commands as well as /.
 - `YOUTUBE_API`:FOR download songs and videos from youtube [not reccamonded]
 - `Message dumb`: nedds
 
### Python dependencies

Install the necessary python dependencies by moving to the project directory and running:

`pip3 install -r requirements.txt`.

This will install all necessary python packages.

### Database

If you wish to use a database-dependent module (eg: locks, notes, userinfo, users, filters, welcomes),
you'll need to have a database installed on your system. I use postgres, so I recommend using it for optimal compatibility.

In the case of postgres, this is how you would set up a the database on a debian/ubuntu system. Other distributions may vary.

- install postgresql:

`sudo apt-get update && sudo apt-get install postgresql`

- change to the postgres user:

`sudo su - postgres`

- create a new database user (change YOUR_USER appropriately):

`createuser -P -s -e YOUR_USER`

This will be followed by you needing to input your password.

- create a new database table:

`createdb -O YOUR_USER YOUR_DB_NAME`

Change YOUR_USER and YOUR_DB_NAME appropriately.

- finally:

`psql YOUR_DB_NAME -h YOUR_HOST YOUR_USER`

This will allow you to connect to your database via your terminal.
By default, YOUR_HOST should be 0.0.0.0:5432.

You should now be able to build your database URI. This will be:

`sqldbtype://EmmaAGroup_bot:pw@Saksham:port/postgres`

Replace sqldbtype with whichever db youre using (eg postgres, mysql, sqllite, etc)
repeat for your username, password, hostname (localhost?), port (5432?), and db name.

### Notice
Keep Credits for [me](https://github.com/MR-SHRLCK) and [prince](https://github.com/Mr-Dark-Prince)
<b> Note one think </b> I waste my many time in front my pc for bring back she.so that's respectable.i know you import or frok this repo and make changes.. that's ok I don't care. But kepp Credits.if you Kang this repo without credits I believe you are a bitch..

[![Deploy To Heroku](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/MR-SHRLCK/ElizabethBot.git)
