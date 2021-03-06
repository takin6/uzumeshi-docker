# uzumeshi-docker #


## Premise
- Install Git  
Refer to "Homebrewとは" in this article  
https://tracpath.com/bootcamp/git-install-to-mac.html  

- Install Ruby 2.6.3 by rbenv  
**Don't forget to change ruby version to 2.6.3  
https://qiita.com/seiyatakahashi/items/1447c401c928d08a040b  

- Install Docker for Mac  
https://docs.docker.com/docker-for-mac/  

- Add public ssh key to github  
http://monsat.hatenablog.com/entry/generating-ssh-keys-for-github  
Tell me your public key personally to me if you wan to contribute!  
email: takayukiinoue116@gmail.com  

- Add ./variables.env  
```
DB_HOST=db
DB_PORT=3306
DB_USERNAME=root
DB_PASSWORD=<custom password>
REDIS_HOST=redis
MONGO_HOST=mongo:27017
REDIS_HOST=redis 
REDIS_SIDEKIQ_URL=redis://redis:6379/0 
REDIS_CABLE_URL=redis://redis:6379/1 
MONGO_HOST=mongo:27017 
LINE_LOGIN_ID=<> 
LINE_LOGIN_SECRET=<>
LINE_CHANNEL_TOKEN=<> 
LINE_CHANNEL_SECRET=<> 
LIFF_URL=<> 
ELASTICSEARCH_URL=http://elasticsearch:9200
```

## Compose Environment
Run Commands
```
$ git clone git@github.com:takin6/uzumeshi-docker.git
$ cd uzumeshi-docker
$ git clone git@github.com:takin6/uzumeshi.git
$ bundle install --path vendor/bundle
$ brew install unison
$ brew install eugenmayer/dockersync/unox
$ docker network create uzumeshi-network

$ bundle exec docker-sync-stack start
``` 


## Docker Commands
```
$ docker-compose exec web bash #start bash process of web container
$ docker container 
```

## When Something Went Wrong  
1. Stop Containers
```
$ docker-compose down
```
