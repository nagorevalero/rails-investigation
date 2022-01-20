# DHH Rails 7 Demo Reversed
This is code repository that was reversed from the original DHH Rails 7 Demo video from Youtube: <https://www.youtube.com/watch?v=mpWFrUwAN88>

## Terminal commands:

 * Setup
   * `rbenv local 2.7.5`
   * `rails _7.0.1_ new demo`
 * Chapter 1: Basic Post Model
   * `rails generate scaffold post title:string content:text`
   * `rails db:migrate`
   * `cat db/schema.rb`
   * `rails server`
 * Chapter 2: Action Text
   * `rails action_text:install` 
   * `bundle install`
   * `rails db:migrate`
 * Chapter 3: Import Map
   * `./bin/importmap pin local-time`