# Hirb-unicode 
`hirb-unicode` fixes the problem that [full-width unicode characters](http://en.wikipedia.org/wiki/Fullwidth_form#Fullwidth_form) is aligned incorrectly.

In the original `hirb` unicode gem, the full-width character will be misaligned: 

![Original hirb screenshot](http://miaout17.github.com/hirb-unicode/hirb-original.png)

With `hirb-unicode-steakknife`, the cells is correctly aligned: 

![Original hirb screenshot](http://miaout17.github.com/hirb-unicode/hirb-unicode.png)

## Installation

    gem install hirb-unicode-steakknife

## Usage

This will load `hirb` and `hirb-unicode-steakknife`, and fix the unicode problem automtically:

    gem 'hirb-unicode-steakknife'
    require 'hirb-unicode-steakknife'

If you are using `bundler` (ex. Rails 3), add `hirb-unicode-steakknife` into your gemfile:

    gem 'hirb-unicode-steakknife'

And run `require 'hirb-unicode-steakknife'` in your irb console or `.irbrc`

## Dependency

`hirb-unicode-steakknife` uses `unicode-display_width` gem to calculate width of unicode characters.

## Testing

* `rake test:hirb` loads `hirb` and `hirb-unicode-steakknife`, run all test of original `hirb` gem. This ensures the original `hirb` functionality is not broken.
* `rake test:unicode` tests functions about unicode string processing.
* `rake test` run both two tests above.

## License

Read MIT-LICENSE file for details.

