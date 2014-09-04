inwx.com XML-RPC Ruby Client
=========
You can access all functions of our frontend via an application programming interface (API). Our API is based on the XML-RPC protocol and thus can be easily addressed by almost all programming languages. The documentation and programming examples in PHP, Java, Ruby and Python can be downloaded here.

There is also an OT&E test system, which you can access via ote.inwx.com. Here you will find the known web interface which is using a test database. On the OTE system no actions will be charged. So you can test how to register domains etc.

Documentation
------
You can view a detailed description of the API functions in our documentation. The documentation as PDF ist part of the Projekt. You also can read the documentation online http://www.inwx.de/en/help/apidoc

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
