# Coding Style

This style is used in the standard library. You can use it in your own project to make it familiar to other developers.

## Naming

__Type names__ are PascalCased. For example:

```ruby
class ParseError < Exception
end

trait Abcd
end

interface Something
end

enum Time
end
```

__Method names__ are camelCased. For example:

```ruby
class Person
  def firstName()
  end

  def dateOfBirth()
  end

  def homepageUrl()
  end
end
```

__Variable names__ are camelCased. For example:

```ruby
class Greeting
  def @defaultGreeting = "Hello world"
  def customGreeting = null

  def new(customGreeting = null)
    @customGreeting = customGreeting
  end

  def printGreeting()
    greeting = @customGreeting or @@defaultGreeting
    trace(greeting)
  end
end
```

__Constants__ are screaming-cased. For example:

```ruby
def LUCKY_NUMBERS = [3, 7, 11]
def GOOGLE_URL = "https://google.com"
```

### Acronyms

In class names, acronyms are _all-uppercase_. For example, `HTTP`, and `LibXML`.

In method names, acronyms are _camelCase_.  For example `#fromJson`,  `#toIo`.

### Directory and File Names

Within a project:

- `/` contains a readme, any project configurations (eg, CI or editor configs), and any other project-level documentation (eg, changelog or contributing guide).
- `<your-project-name/` contains the project's source code.
- `bin/` contains any executables.

File paths match the namespace of their contents. Files are named after the class or namespace they define.

For example, `myproject.MyModule` is defined in `myproject/MyModule.rx`.

## Whitespace

Use __two spaces__ to indent code inside namespaces, methods, blocks or other nested contexts. For example:

```ruby
class Parser
  def parse(scoreText)
    try
      # Parse something
    catch(err : ParseError)
      # handle error ...
    end
  end
end
```

Within a class, separate method definitions and constants with __one newline__. For example:

```ruby
class Money  
  def @CURRENCIES = {
    ["EUR"] = 1.0,
    ["ARS"] = 10.55,
    ["USD"] = 1.12,
    ["JPY"] = 134.15,
  }
  
  def new(currency, value)
  end
  
  def amount
    # implement conversion ...
  end
end
```