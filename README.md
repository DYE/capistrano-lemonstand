capistrano-lemonstand
=====================

Setup and deploy a LemonStand e-Commerce application onto a unix server using the Capistrano-deployless Ruby lib.

# 

Capistrano is primarily a Ruby on Rails (RoR) deployment tool, so to use this deployment process you will need to use the https://github.com/leehambley/railsless-deploy/ gem instead of the default Capistrano gem.

## Installation of RubyGems and railsless-deploy

    # gem install railsless-deploy

## Usage

Setup your LemonStand application to use Railsless Deploy of Capistrano

    # capify .

Open your application's `Capfile` and make it begins like this:

    require 'rubygems'
    require 'railsless-deploy'
    load    'config/deploy'

Taking care to remove the original `require 'deploy'` as this is where all the standard tasks are defined.

You should then be able to proceed as you would usually, you may want to familiarise yourself with the truncated list of tasks, you can get a full list with:

    $ cap -T

## What's in the box?

If you want to try before you buy, here's the list of tasks included with this version of the deploy recipe:

    cap deploy               # Deploys your project.
    cap deploy:check         # Test deployment dependencies.
    cap deploy:cleanup       # Clean up old releases.
    cap deploy:cold          # Deploys and starts a `cold' application.
    cap deploy:pending       # Displays the commits since your last deploy.
    cap deploy:pending:diff  # Displays the `diff' since your last deploy.
    cap deploy:rollback      # Rolls back to a previous version and restarts.
    cap deploy:rollback:code # Rolls back to the previously deployed version.
    cap deploy:setup         # Prepares one or more servers for deployment.
    cap deploy:symlink       # Updates the symlink to the most recently deployed ...
    cap deploy:update        # Copies your project and updates the symlink.
    cap deploy:update_code   # Copies your project to the remote servers.
    cap deploy:upload        # Copy files to the currently deployed version.
    cap invoke               # Invoke a single command on the remote servers.
    cap shell                # Begin an interactive Capistrano session.


## Bugs & Feedback

Fork the project and submit a Pull Request