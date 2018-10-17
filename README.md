### Abracadabra
---

https://github.com/TrevorHinesley/abracadabra

```
gem 'abracadabra'
bundle
gem insall abracadabra

```

```ruby
click_to_edit @friend, path: friend_path(@friend), attribute: :name, deletable: true

click_to_edit @friend,
  path: friend_path(@friend),
  attribute: :name,
  class: "my-abracadabra-#{index}",
  id: "my-abracadabra-#{index}",
  value: @friend.name.titleize,
  method: :put,
  buttonless: true,
  type: :json,
  deletable: "Are you sure?",
  deletable_path: user_friend_path(@friend),
  deletable_type: :json
  tab_to_next: "#my-abracadabra-#{index+1}",
  submit_on_blur: true
  
def execute_abracadabra value, selector = ".abracadabra"
  page.execute_script("$(\"#{selector}\").click();")
  page.execute_script("$(\".abracadabra-input\").val(\"#{value}\");")
  page.execute_script("$(\".abracadabra-submit\").click();")
end

execute_abracadabra "new value", "#editable-name"

```

```js
*= require abracadabra
@import "abracadabra-scss";
//= require abracadabra

$.abracadabra();

abracadabraSubmitIcon = "fa fa-check";
abracadabraCancelIcon = "fa fa-times";
abracadabraDeleteIcon = "fa fa-times-circle-o";
```

```html
<%= click_to_edit @user, path: user_path(@user), attribute: :name %>

```


