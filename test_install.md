# Install testing Rspec & Capybara

https://github.com/teamcapybara/capybara
https://github.com/rspec/rspec-rails

### Add to Gemfile:

- `gem 'rspec-rails', '~> 6.0.0'`
- `gem 'capybara'`

### Rspec install:

`rails generate rspec:install`

### Capybara instructions (Campus Code):

Para configurar corretamente a execução do Capybara, dentro do arquivo spec/rails_helper.rb, lembre-se de procurar o bloco que começa com `RSpec.configure do |config|` e dentro dele adicionar:

```ruby
config.before(type: :system) { driven_by(:rack_test) }
```

### Capybara methods

https://devhints.io/capybara
https://rubydoc.info/github/teamcapybara/capybara/master/Capybara/RSpecMatchers

### RSpec folder structure

https://relishapp.com/rspec/rspec-rails/v/6-0/docs/directory-structure
