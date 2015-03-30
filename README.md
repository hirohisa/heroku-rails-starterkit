# ruby-getting-started

## Documentation

- [github heroku](https://github.com/heroku/ruby-getting-started)
- [devcenter.heroku.com](https://devcenter.heroku.com/articles/getting-started-with-ruby)

## Getting started with Rails4 on Mac OS X in local

- Install the [Heroku Toolbelt](https://toolbelt.heroku.com/).
- Install [Homebrew](https://github.com/Homebrew/homebrew) and [rbenv](https://github.com/sstephenson/rbenv)
  ```
  $ brew update
  $ brew install rbenv ruby-build
  ```

- Install ruby 2.2.0 (available 2.2.0 for Rails4)
  ```
  $ rbenv install -v 2.2.0
  ```

- Use ruby 2.2.0
  ```ruby
  $ rbenv local 2.2.0 #echo '2.2.0' > .ruby-version
  $ echo 'eval "$(rbenv init -)"' >> ~/.bash_profile
  $ ruby -v
  # ruby 2.2.0p0 (2014-12-25 revision 49005) [x86_64-darwin14]
  ```

- Write in Gemfile
  ```ruby
  ruby '2.2.0'
  ```

- Install and run bundle for ruby 2.2.0
  ```
  $ gem install bundle
  $ bundle install --path vendor/bundle
  ```

## which

- Check command's path

  ```
  $ rbenv which ruby
  # .rbenv/versions/2.2.0/bin/ruby
  $ rbenv which gem
  # .rbenv/versions/2.2.0/bin/gem
  $ rbenv which bundle
  # rbenv: bundle: command not found
  $ rbenv which bundle
  # .rbenv/versions/2.2.0/bin/bundle
  ```

## Postgres

- Run
  ```
  $ postgres -D /usr/local/var/postgres
  ```

## errors

- forget to install postgres

  ```
  An error occurred while installing pg (0.17.1), and Bundler cannot continue.
  Make sure that `gem install pg -v '0.17.1'` succeeds before bundling.
  ```

  ```
  $ brew install postgresql
  $ initdb /usr/local/var/postgres -E utf8
  ```
