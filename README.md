# Heroko Command Line Installation for Linux Ubuntu

- Check uname -m, find if X86_64 or X86; if say x64 then

```
wget https://cli-assets.heroku.com/heroku-cli/channels/stable/heroku-cli-linux-x64.tar.gz -O heroku.tar.gz

tar -xvzf heroku.tar.gz

mkdir -p /usr/local/lib /usr/local/bin
```

- Now find the eact name of the file downloaded using
```
ls 
```
 - copy the 'heroku-cli-XXXXXX' file name
 
 
 mv heroku-cli-XXXXXX /usr/local/lib/keroku
 
 for example
 
 ```
 sudo mv heroku-cli-v6.13.12-c65a3c3-linux-x64 /usr/local/lib/heroku
 
```

- ensure you have a space before /usr/local.lib/heroku

```
sudo mv heroku-cli-v6.13.12-c65a3c3-linux-x64 /usr/local/lib/heroku

sudo ln -s /usr/local/lib/heroku/bin/heroku /usr/local/bin/heroku
```
