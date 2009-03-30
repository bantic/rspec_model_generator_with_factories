# ModelGeneratorWithFactories

This is a modification of the standard rspec_model generator (from [http://wiki.github.com/dchelimsky/rspec/rails](Rspec_Rails gem)) to generate spec tests instead of unit tests and factory definitions for use with [factory_girl](http://github.com/thoughtbot/factory_girl) instead of fixtures.

## Requirements

This generator will only be useful with factory_girl version 1.1.4 or later. The generated code will not fail if version 1.1.4 is not installed; the factories will just not be available to your tests.

You will still need to add `require 'factory_girl'` to your test environment. This generator will not do that for you.

## Installation

To install the generator as a plugin in your Rails app:

    ./script/plugin install git://github.com/bantic/rspec_model_generator_with_factories.git

This will override the standard Rspec-Rails rspec_model generator for this application. You can also pull the `generators/rspec_model` directory out of this repository and put it in `$HOME/.rails/generators` to make it available to all your present and future Rails applications.

## Usage

Usage is the same as the standard Rails model generator:

    ./script/generate rspec_model Thing name:text description:text

After generating the model, look in `test/factories` for your factory definition and in `spec/models` for the spec.

## Author/Copyright

This generator incorporates most of its code from the stock Rails model generator, which is:

Copyright (c) 2004-2008 David Heinemeier Hansson

The modifications to make the generator generate factories instead of fixtures are:

Copyright (c) 2008 Mark Cornick and Viget Labs

Both the original Rails code and the modifications are released under the MIT license.

The modifications to make the generator generate spec tests instead of unit tests are:

Copyright (c) 2009 Cory Forsyth and outside.in