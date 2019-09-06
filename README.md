<p align="center">
  <a href="https://www.inwx.com/en/" target="_blank">
    <img src="https://images.inwx.com/logos/inwx.png">
  </a>
</p>

INWX Domrobot Ruby Client
=========
You can access all functions of our frontend via our API, which is available via the XML-RPC or JSON-RPC protocol and thus can be easily consumed with all programming languages.

There is also an OT&E test system, which you can access via [ote.inwx.com](https://ote.inwx.com/en/). Here you will find the known web interface which is using a test database. On the OT&E system no actions will be charged. So you can test as much as you like there.

Documentation
------
You can view a detailed description of the API functions in our documentation. You can find the online documentation [by clicking here](https://www.inwx.de/en/help/apidoc).

If you still experience any kind of problems don't hesitate to contact our [support via email](mailto:support@inwx.de).

Example
-------

```ruby
require "inwx/Domrobot"
require "yaml"

addr = "api.ote.domrobot.com"
# addr = "api.domrobot.com"
user = "your_username"
pass = "your_password"

domrobot = INWX::Domrobot.new(addr)

result = domrobot.login(user,pass)
puts YAML::dump(result)

object = "domain"
method = "check"

params = { :domain => "mydomain.com" }

result = domrobot.call(object, method, params)

puts YAML::dump(result)
```

You can also look at the example.rb in the Project.

License
----

MIT
