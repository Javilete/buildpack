Heroku Buildpack for Scala [![Build Status](https://travis-ci.org/heroku/heroku-buildpack-scala.svg?branch=master)](https://travis-ci.org/heroku/heroku-buildpack-scala)
=========================

This is a custom buildpack for Scala to add the sass compilation process for the style of the app during the build process.

The code added in the compile file is the following, which runs the sass gems to be able to compile all the scss files in the app:

mkdir -p $CACHE_DIR/.gems
gem install -i $CACHE_DIR/.gems --no-rdoc sass
export PATH=$PATH:$CACHE_DIR/.gems/bin
export GEM_PATH=$GEM_PATH:$CACHE_DIR/.gems




