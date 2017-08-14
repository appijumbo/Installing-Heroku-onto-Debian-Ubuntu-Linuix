# Heroko Command Line Installation for Linux Ubuntu

1) Go into the Downloads directory

```
cd ~/Downloads
```

2) Check uname -m, find if X86_64 or X86; and make a note of it (assumed x64 for this description) 

3) get the x64 from the website url ie wget

4) extract the tarball

5) make sure parent directorys exist, make them if they don't /usr/local/lib and /usr/local/bin no errors if exiisting

```
wget https://cli-assets.heroku.com/heroku-cli/channels/stable/heroku-cli-linux-x64.tar.gz -O heroku.tar.gz

tar -xvzf heroku.tar.gz

mkdir -p /usr/local/lib /usr/local/bin
```

6) Now find the exact name of the file downloaded

```
find ~/Downloads -name heroku-cli*
```

7) as superuser, move the 'heroku-cli-XXXXXX' file into /usr/local/lib/heroku
 
mv heroku-cli-XXXXXX /usr/local/lib/heroku
 
for example
 
```
 sudo mv heroku-cli-v6.13.12-c65a3c3-linux-x64 /usr/local/lib/heroku
 
```

( just ensure you have a space before /usr/local.lib/heroku)

8) Finally make a symbolic link

```
sudo ln -s /usr/local/lib/heroku/bin/heroku /usr/local/bin/heroku
```
