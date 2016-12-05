**Action Cable with Devise**: <https://github.com/lab2019/actioncable-examples>

# Quick

* `$ sudo service redis-server start`: servis bir süre sussa bile cronjob üzerinden işlem daha sonradan tamamlanıyor.
* `$ rails s` 
* `$ ./bin/cable`

# Action Cable Examples

A collection of examples showcasing the capabilities of Action Cable.

## Dependencies

You must have redis installed and running on the default port:6379 (or configure it in config/redis/cable.yml).

### What/how/why is Redis?

* Redis is an in-memory key-value store known for its flexibility, performance, and wide language support.

### Installing Redis
##### On Ubuntu 16.04

* `sudo apt-get install redis-server`

##### On Linux
* `wget http://download.redis.io/redis-stable.tar.gz`
* `tar xvzf redis-stable.tar.gz`
* `cd redis-stable`
* `make`
* `make install`

##### On Mac
* `brew install redis`

###### Note: You must have Ruby 2.2.2 installed in order to use redis

### Configure Redis

* `sudo vim /etc/redis/redis.conf`
* https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-redis-on-ubuntu-16-04#download,-compile,-and-install-redis

### Test

* `$ redis-server`
* `$ redis-cli`

### How to use

* https://www.digitalocean.com/community/tutorials/how-to-install-and-use-redis

## Starting the servers

1. Run `./bin/setup`
2. Open up a separate terminal and run: `./bin/rails server`
3. Run `./bin/cable`
4. One more terminal to run redis server: `redis-server`
4. Visit `http://localhost:3000`

## Live comments example

1. Open two browsers with separate cookie spaces (like a regular session and an incognito session). 
2. Login as different people in each browser. 
3. Go to the same message.
4. Add comments in either browser and see them appear real-time on the counterpart screen.

![Live comments example](/example.gif?raw=true "Live comments example")


# Link
- Heroku deploy: <https://blog.heroku.com/real_time_rails_implementing_websockets_in_rails_5_with_action_cable>
- Heroku deploy-another: <http://www.thegreatcodeadventure.com/deploying-action-cable-to-heroku/>
