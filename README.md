Guess The Friend
================

This is a complete Rails app developed in 48 hours during the 2012 [Rails Rumble](http://railsrumble.com), in
the context of the [48Rails](http://48rails.it)

It implements the classic [Guess The Friend](http://player.vimeo.com/video/1193166?title=1&byline=1&portrait=1)
game, picking the choices from your recently contacted Facebook friends, getting their details and giving you
hints :smile:.

Everything is in the RailsRumble aftermath state - so don't expect clean code and full coverage - it is left
here just for posterity :smiley:.

App setup
----------

* Clone the repo
* mkdir `log/`
* Configure `config/database.yml` using `config/database.yml.example` as a template
* Run `bundle`
* Run `rake db:setup`
* Run `rails server`

Facebook setup
--------------

* Create a new facebook app and assign it a domain. Say, `example.com`
* Create `config/config.yml` using `config/config.example.yml` as a template
* Add `127.0.0.1 guesswho.example.com` to your `/etc/hosts` (as root)
* Go to http://guesswho.example.com:3000/

App deploy
----------

* Set up `config/deploy.rb` for your server - the current config assumes
  there's a `guesswho` user on it and a process manager keeping an `unicorn`
  up. An example `upstart` configuration is in `config/upstart.conf`.
* cap deploy
* If you want to deploy another branch, use `cap -S branch=foobar deploy`

Authors
-------

* Andrea Pavoni [@apeacox](https://github.com/apeacox)
* Alessandro Vendruscono [@vendruscolo](https://github.com/vendruscolo)
* Claudio Floreani [@ClaudioFloreani](https://github.com/ClaudioFloreani)
* Marcello Barnaba [@vjt](https://github.com/vjt)
