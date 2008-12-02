# ModelGeneratorWithFactories

This is a modification of the standard Rails model generator (from Rails 2.2.2) to generate factory definitions for use with [factory_girl](http://github.com/thoughtbot/factory_girl) instead of fixtures.

## Requirements

This generator will only be useful with factory_girl version 1.1.4 or later. The generated code will not fail if version 1.1.4 is not installed; the factories will just not be available to your tests.

You will still need to add `require 'factory_girl'` to your test environment. This generator will not do that for you.

## Installation

1. Create a directory `$HOME/.rails/generators` if you have not already.
2. Change to that directory and run `git clone git://github.com/vigetlabs/model_generator_with_factories.git model_with_factories`
3. If you want this generator to override the standard Rails model generator, `mv model_with_factories model`

## Usage

If you only did steps 1 and 2 of the installation:

    ./script/generate model_with_factories Thing name:title description:text`

If you also did step 3:

    ./script/generate model Thing name:title description:text`

After generating the model, look in `test/factories` for your factory definition. As with fixtures in the stock model generator, you will probably want to change some of the default values.

## Author/Copyright

This generator incorporates most of its code from the stock Rails model generator, which is:

Copyright (c) 2004-2008 David Heinemeier Hansson

The modifications to make the generator generate factories instead of fixtures are:

Copyright (c) 2008 Mark Cornick and Viget Labs

Both the original Rails code and the modifications are released under the MIT license.
