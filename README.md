Just Another (Django) Blog
==========================

Yes, it's another Django blog.  Not a blogging framework, though --just a blog.
No bells or whistles.  Designed to just get up and running with a basic blog as
quickly as possible.  No comments, no categories, no tagging.  Themes are all
template-based.

Getting started
---------------

* You'll need Django installed, and some way of hosting it -- the default
  runserver, Apache with mod_wsgi, or (of course) a
  [PythonAnywhere](http://www.pythonanywhere.com) account.
* You'll also need the
  [South Django migrations package](http://south.aeracode.org/): if you're on
  PythonAnywhere, you'll have it already. If not, `pip install south`.
* `git checkout git://github.com/resolversystems/jab.git`
* `cd jab`
* `cp local_settings_template.py local_settings.py`
* Edit `local_settings.py`, and change the variables in there to point to an
  appropriate database etc.  The Twitter and email fields are optional, just
  miss them out if you don't want to use them.
* `python manage.py syncdb`
* `python manage.py migrate`

...and you're done!  Log in to the admin GUI using the admin username you
created during the syncdb, and add Post objects to post; set the status to
"Published" when you want a post to go live.

If you want to add something to the header (like, say, an "About" page) then set
the "Link from header" checkbox to true -- and you might want to also set the
"Show in list and rss" checkbox to false.