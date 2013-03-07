<h1>Pari</h1>


P.Sainath's People's Archive Of Rural India
[![Build Status](https://travis-ci.org/RuralIndia/pari.png)](https://travis-ci.org//RuralIndia/pari)


Dev Setup
==========

* clone the repo.
* Use [pythonbrew](https://github.com/utahta/pythonbrew) for python runtime and packages management

<pre>
pythonbrew install 2.7.3
ptyhonbrew use 2.7.3
pythonbrew venv create pari
pythonbrew venv use pari
</pre>

* Install the dependencies
<pre>
pip install -r requirements.txt
</pre>
* Setup the database
<pre>
python manage.py syncdb --all  --noinput 
python manage.py migrate --fake
python manage.py loaddata pari/fixtures/initial_content.json 
python manage.py runserver
</pre>

<b>Note:</b> Add these to your .bash_profile if you are getting "unknown locale: UTF-8" error
<pre>
export LC_CTYPE=en_US.UTF-8
export LC_ALL=en_US.UTF-8
</pre>
