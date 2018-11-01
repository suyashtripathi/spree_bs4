# spree_bs4

This extension removes the Bootstrap 3 CSS and Javascript from the frontend of your Spree 3.X project, and then inserts Bootstrap 4 CSS and Javascript back into the frontend ready for use.

Please be aware that you will need to pick through your Spree frontend view files replacing the old Bootstrap 3 classes with the relevant Boostrap 4 classes.

The extension was designed with the assumption that you will be doing some web design to entirely customise the look and feel of your Spree store, and therefor we make no attempt to render a pretty view out of the box.

If you find any problems while using this extension please raise an issue, or fork the project, fix/update/improve and then submit a pull request.

## Installation

1. Add these lines to the bottom of your Gemfile:
  ```ruby
  gem 'spree_remove_bs3', github: 'matthewkennedy/spree_remove_bs3'
  gem 'spree_bs4', github: 'matthewkennedy/spree_bs4'
  ```

2. Install the gem using Bundler:
  ```ruby
  bundle install
  ```

3. Copy & run the following commands in order
  ```ruby
  bundle exec rails g spree_remove_bs3:install
  bundle exec rails g spree_bs4:install
  ```

4. Restart your server

  If your server was running, restart it so that it can find the assets properly.
  
  That is it, you should have a Spree 3.X project with a fully working **Bootstrap 3 Admin** interface and a **Frontend with Bootstrap 4** CSS and JS.

## Testing

First bundle your dependencies, then run `rake`. `rake` will default to building the dummy app if it does not exist, then it will run specs. The dummy app can be regenerated by using `rake test_app`.

```shell
bundle
bundle exec rake
```

When testing your applications integration with this extension you may use it's factories.
Simply add this require statement to your spec_helper:

```ruby
require 'spree_bs4/factories'
```


## Contributing

If you'd like to contribute, please take a look at the
[instructions](CONTRIBUTING.md) for installing dependencies and crafting a good
pull request.

Copyright (c) 2018 [name of extension creator], released under the New BSD License
