-   in Gemfile

    add `gem "importmap-rails"`

    add `gem 'turbo-rails'`

    add `gem 'stimulus-rails'`

Run:

```bash
    $ rails importmap:install
    $ rails turbo:install
    $ rails stimulus:install
    $ rails hotwire:install
    $ rails hotwire:install
```

---

Aplication view (If no present)

```html
<%= stylesheet_link_tag "application", "data-turbo-track": "reload" %> <%=
javascript_importmap_tags %>
```
