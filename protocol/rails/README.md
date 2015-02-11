Rails Protocol
==============

A guide for writing great web apps.

Set Up App
----------

Get the code.

    git clone git@github.com:organization/app.git

Use [Heroku config](https://github.com/ddollar/heroku-config) to get `ENV`
variables.

    heroku config:pull --remote staging

Git Protocol
------------

Follow the normal [Git Protocol](/protocol/git).

Product Review
--------------

Follow the normal [Product Review protocol](/protocol/product-review).

Code Review
-----------

Follow the normal [Code Review guidelines](/code-review). When reviewing others'
Rails work, look in particular for:

* Review whether new database indexes are necessary if new columns or SQL
  queries were added.
* Review whether new scheduler (`cron`) tasks have been added and whether there
  is a related todo in the project management system to add it during the
  staging and production deploys.

Deploy
------

View a list of new commits. View changed files.

    git fetch staging
    git log staging/master..master
    git diff --stat staging/master

If necessary, add new environment variables.

    heroku config:add NEW_VARIABLE=value --remote staging

Deploy to [Heroku](https://devcenter.heroku.com/articles/quickstart).

    git push heroku master

If necessary, run migrations and restart the dynos.

    heroku run rake db:migrate --remote staging
    heroku restart

Test the feature in browser.
