# Heroko Command Line Installation for Linux Ubuntu

I had problems installing Heroku command line for Ubuntu Linux [using their one line installation](https://devcenter.heroku.com/articles/heroku-cli#debian-ubuntu) 
I reverted to Heroku's linux installation alternative [standalone](https://devcenter.heroku.com/articles/heroku-cli#standalone) method which requires a bit more work, and decided to break down the steps a little more just in case it help someone out there.


* Go into the Downloads directory

```
cd ~/Downloads
```

* Check uname -m, find if X86_64 or X86; and make a note of it (X86_64 assumed for this description, or just x64 for short) 
```
uname -m
```

* Assuming its X64 for this description, get the x64 from the website url using 'wget'

```
wget https://cli-assets.heroku.com/heroku-cli/channels/stable/heroku-cli-linux-x64.tar.gz -O heroku.tar.gz
```

* extract the tarball
```
tar -xvzf heroku.tar.gz
```

* make sure parent directories exist, make them if they don't /usr/local/lib and /usr/local/bin no errors if existing

```
mkdir -p /usr/local/lib /usr/local/bin
```

* Now find the exact name of the file downloaded

```
find ~/Downloads -name heroku-cli*
```

* as superuser, move the 'heroku-cli-XXXXXX' file into /usr/local/lib/heroku

( just ensure you have a space before /usr/local.lib/heroku)
 
```
 sudo mv heroku-cli-v6.13.12-c65a3c3-linux-x64 /usr/local/lib/heroku
 
```

8) Finally make a soft link

```
sudo ln -s /usr/local/lib/heroku/bin/heroku /usr/local/bin/heroku
```
