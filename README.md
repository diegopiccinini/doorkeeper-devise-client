# Dookreeper Devise+Omniauth Client

This app is an example of OAuth2 client. It is a copy of [doorkeeper-devise-client](https://github.com/doorkeeper-gem/doorkeeper-devise-client)
to run easy with one OAuth2 doorkeeper provider in rails 4.2.5
You can download the provider example [here](https://github.com/diegopiccinini/doorkeeper-provider)

## About Doorkeeper Gem

For more information [about the gem](https://github.com/applicake/doorkeeper),
[documentation](https://github.com/applicake/doorkeeper#readme),
[wiki](https://github.com/applicake/doorkeeper/wiki/_pages) and another resources,
check out the project [on GitHub](https://github.com/applicake/doorkeeper).

## Installation & Configuration

If you want to run the application by yourself here are the steps for
you.

First you need to clone the [repository from GitHub](https://github.com/diegopiccinini/doorkeeper-devise-client)

    git clone git@github.com:diegopiccinini/doorkeeper-devise-client.git

Install all the gems

    bundle install

And migrate the databse

    rake db:migrate

At this point the application should be ready to run, but it won't
communicate correctly with the provider. You need to set up environment
variables to indicate the oauth2 provider values. I added dotenv gem to help to set up
the environemnt variables in your .env file.There is a .env.example file
to set these values

    DOORKEEPER_APP_ID = "375c2e3fd..." # ID for your app registered at the provider
    DOORKEEPER_APP_SECRET = "6a2fa82ab..." # Secret
    DOORKEEPER_APP_URL = "http://localhost:4000" # URL to the provider

You have to create your .env to set the values in the development environment

Now you are ready to start the app

    rails s


