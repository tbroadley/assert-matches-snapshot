# `assert_matches_snapshot`

An assertion for snapshot testing. Take a snapshot of `response.body` at any point during a Rails functional or integration test. If the contents of `response.body` later change, the assertion will fail.

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'assert_matches_snapshot'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install assert_matches_snapshot

## Usage

Add the following to any Rails functional or integration test:

```ruby
assert_matches_snapshot 'after page is loaded'
```

`assert_matches_snapshot` takes one argument: a string that is used to distinguish snapshots from each other. This string should be unique across all tests for a controller-action combination.

To overwrite the snapshots, set the environment variable `OVERWRITE_SNAPSHOTS=true` before running your test command.

## Development

After checking out the repo, run `bundle install` to install dependencies. Then, run `rake test` to run the tests, or `bundle exec guard` to run the tests every time a file is changed.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/tbroadley/assert_matches_snapshot.

## License

The gem is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).
