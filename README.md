Rails Code Snippets
=================

This contains a list of all useful code snippets that i have used and aggregated over my time developing Rails based applications.

##Ruby Rails Code


1. Use the link_to_active_state gem to make active any link when selected, usually seen in nav bars. Use the following to add to your nav bars </li>

```rails
<%= link_to "Sign in", new_user_session_path, active_on: new_user_session_path %>

```
2. If you need to add a bootstrap icon in your button

* As part of your form


```ruby

<%= button_tag(type: 'submit', class: "btn btn-success") do %>
    <i class="icon-ok icon-white"></i> Signup
  <% end %>
  
```

* Normal way ( here you can see i don use the bootstrap provided icons, use fontello for its large collections)


```
<%= link_to "<i class=\"fontello-icon-off \"></i>".html_safe,
          destroy_user_session_path,
          class: "btn btn-danger", :'data-toggle' => "popover", :title => "Sign Out",
          method: :delete %>
```


