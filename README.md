# Pub Lunch

## at Big Heroku Tavern

This installs dependend dart packages, using darts package manager `pub`.
This script is configured to work on Heroku by default, using [this build-pack](https://github.com/kohlikohl/heroku-buildpack-dart) 

## Getting Started

The easiest would be to download the file here.
Place it into the root directory of your dart app and add following to your `Procfile` if you run your dart app on Heroku

```
web: bash server
```

You can of course run this script any other way.

## Configuration
You can specify the location of the dart binaries and the name of the file including the `main()` function by specifying environmental variables.
On Heroku this works like that:

```bash
# Setting path of dart binaries
$> heroku config:set DART_BINARY=<path to binary> #defaults to './dart-sdk/bin'

# Setting name of file which includes main()
$> heroku config:set MAIN_FILE=<name of file excluding .dart> #defaults to 'main'
```

## License

The MIT License - Copyright (c) 2012 Matthias Knoll