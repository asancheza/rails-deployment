# Rails deployment

Documentation to create and deploy Rails applications in local and Heroku.

## Create app
```
rails new sample_app
```

## Default Gemfile
```
source 'https://rubygems.org'

gem 'rails',        '4.2.2'
gem 'sass-rails',   '5.0.2'
gem 'uglifier',     '2.5.3'
gem 'coffee-rails', '4.1.0'
gem 'jquery-rails', '4.0.3'
gem 'turbolinks',   '2.3.0'
gem 'jbuilder',     '2.2.3'
gem 'sdoc',         '0.4.0', group: :doc

group :development, :test do
  gem 'sqlite3',     '1.3.9'
  gem 'byebug',      '3.4.0'
  gem 'web-console', '2.0.0.beta3'
  gem 'spring',      '1.1.3'
end

group :production do
  gem 'pg',             '0.17.1'
  gem 'rails_12factor', '0.0.2'
```

## Install bundle
```
bundle install --without production
```

## Generate controller with different views
```
rails generate controller controller index links about
```

## Create branches and merge
```
git checkout -b sass-erb-static # create branch
git checkout master # checkout master
git merge sass-erb-static # our branch
```

## Create app in Heroku
```
heroku create
```

## Push repo and Heroku
```
git push -u origin master
git push heroku master
```

## Debug in Heroku
```
heroku run rails console
```
