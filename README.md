# Rails5MySql5.6
make an environment of
- Ruby 2.3.1
- Rails 5
- MySQL 5.6

# pull this repository
```
git clone git@github.com:miyasue/Rails5MySql5.6.git
```

# create rails app
```
docker-compose run web rails new . --force --database=mysql --skip-bundle
```

# edit Gemfile
```
gem 'therubyracer', platforms: :ruby
```

# build
```
docker-compose build
```

# edit config/database.yml
```
default: &default
  adapter: mysql2
  encoding: utf8
  pool: 5
  username: root
  password: root
  host: db
```

# up
```
docker-compose up
```


# create database
```
docker-compose run web rake db:create
```
