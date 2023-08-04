# Trailblazer::Pro::Rails

## Installation

In your Rails' `Gemfile`.

```ruby
gem "trailblazer-pro-rails"
```

## Usage

1. Get your API key from https://pro.trailblazer.to
2. Run our generator and enter your API key.
    ```
    $ rails g trailblazer:pro:install

    ```
3. Run your operation via `#wtf?`.
    ```ruby
    result = API::V1::Diagram::Operation::Update.wtf?(params: params)
    ```

4. Click the `[TRB PRO]` link in your terminal and start debugging.

![Our web debugger in action.](docs/debugger-ide-screenshot-august.png)

Note: we're currently playing with various invocation styles and at some point you might not even have to use `Operation.wtf?` anymore.



## Testing

Currently, from the top directory, you need to run

```ruby
$ rake test_1
```
This will test the generator on a new Rails app in isolation.

```ruby
$ rake test_2
```

Tests if `wtf?` works without any PRO configuration, but PRO is added.


### Architecture

* One `Gemfile` for all scenarios on `test/dummies`
