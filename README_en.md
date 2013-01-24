# Motion::Pixate::Observer

This gem provides a function that you changes css files, apply changes into your application that uses Pixate Framework immediately.

You do not need rebuild your application and any operations.
Only update your css files.

## Requirements

- RubyMotion 1.0 or greater (see http://www.rubymotion.com).
- Pixate Framework 1.0 or greater (see http://www.pixate.com/).

## Installation

```
$ gem install motion-pixate-observer
```

## Usage

- Add require `motion-pixate-observer` to your `Rakefile`

```ruby
require 'rubygems'
require 'motion-pixate-observer'
```

- include `Motion::Pixate::Observer` in Main Controller. Call `startObserving` in `viewDidLoad`.

```ruby
class MainViewController < UIViewController
  include Motion::Pixate::Observer  # include Motion::Pixate::Observer in Main Controller

  def viewDidLoad
    super

    startObserving # start searching and communicate with server

    ....
  end
```

- First, you have to start server. Depends on MacRuby when start server.

```
$  ./pixate_server css_file_path
```

After started server, run your RubyMotion application.

- update css files, apply changes immediately.
