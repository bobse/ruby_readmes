# Devise for Rails 7

https://github.com/heartcombo/devise#starting-with-rails

## Instalation:

- Add `gem 'devise'` to Gemfile
- `$ rails generate devise:install`
- Add this line to `config/environments/development.rb`

  ```ruby
  config.action_mailer.default_url_options = { host: "localhost", port: 3000 }
  ```

- Generating the model:

  `rails generate devise <model-name> <extra-fields>`

  ex: `rails generate devise user name:string`

- `rails db:migrate`

- Be sure to have rootpath set in your routes
