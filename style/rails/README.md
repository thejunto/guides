Rails
=====

* Name date columns with `_on` suffixes.
* Name datetime columns with `_at` suffixes.
* Name time columns (referring to a time of day with no date) with `_time`
  suffixes.
* Name initializers for their gem name.
* Order ActiveRecord associations above ActiveRecord validations.
* Order controller contents: filters, public methods, private methods.
* Put application-wide partials in the [`app/views/application`] directory.
* Use the default `render 'partial'` syntax over `render partial: 'partial'`.
* Use `link_to` for GET requests, and `button_to` for other HTTP verbs.

[`app/views/application`]: http://asciicasts.com/episodes/269-template-inheritance

Migrations
----------

[Sample](migration.rb)

* Set an empty string as the default constraint for non-required string and text
  fields. [Example][default example].

[default example]: migration.rb#L6

Routes
------

* Avoid the `:except` option in routes.
* Use the `:only` option to explicitly state exposed routes.

Email
-----

* Use the user's name in the `From` header and email in the `Reply-To` when
  [delivering email on behalf of the app's users].

[delivering email on behalf of the app's users]: http://robots.thoughtbot.com/post/3215611590/recipe-delivering-email-on-behalf-of-users
