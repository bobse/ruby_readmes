# Setting up Active Storage:

https://pragmaticstudio.com/tutorials/using-active-storage-in-rails
https://guides.rubyonrails.org/v6.0.0/active_storage_overview.html

- Inside `config/application.rb`

  ```ruby
  #Uncoment this line
  require "active_storage/engine"
  ```

- Create a folder storage in your root project folder
- Create a file storage.yml in /config

  ```yaml
  local:
    service: Disk
    root: <%= Rails.root.join("storage") %>
  ```

- In /environments/development.rb add:

  ```ruby
  config.active_storage.service = :local
  ```

## Using Active Storage:

- Inside your model file add:

  ```ruby
  has_one_attached :image_name
  ```

- Upload button:
  ```ruby
  <%= f.label :image_name %>
  <%= f.file_field :image_name %>
  ```
- Display image:
  ```ruby
  <%= image_tag event.image_name %>
  ```
