# jpb_doc_code_tut
```bash
Inspired from: Sphinx & Read the Docs: https://www.youtube.com/watch?v=oJsUvBQyHBs

$ mkdir jpb_doc_code_tut
$ cd jpb_doc_code_tut/
$ echo "# jpb_doc_code_tut" >> README.md
$ git init
$ git add README.md
$ git commit -m "first commit"

$ git remote add origin https://github.com/jpbourrely/jpb_doc_code_tut.git
$ git push -u origin master

$ # create associated project in ReadTheDocs - automatic GitHub webhook creation (in GitHub)

$ mkdir project_1
$ mkdir project_2
$ mkdir docs
$ touch .gitignore
$ cd docs

$ sphinx-quickstart
$ ls
Makefile	_build		_static		_templates	conf.py		index.rst

$ cd ..
$ vi .gitignore # on rajoute de gitignore.io + _build _static _templates (de sphinx-quickstart)
$ git status
$ git add .
$ git status
$ git commit -am "first commit"
[master 53baf72] first commit
$ git status
$ git push origin master
$ cd docs
$ cd docs
$ make html
$ open _build/html/index.html 
$ cd ..

$ # add badge in index.rst
$ git add .
$ git commit -am "add readthedocs badge"
$ git push origin master

$ cd docs
$ vi conf.py # add sphinx_rtd_theme 
$ make html
$ pip install sphinx_rtd_theme
$ make html
$ open _build/html/index.html 
$ vi help.rst
$ vi license.rst
$ vi index.rst 
$ make html
$ open _build/html/index.html 
$ cd ..
$ git status
$ git add .
$ git commit -am "add hel and license files"
$ git push origin master

$ cd project_1
$ touch __init__.py
$ touch factorial.py
$ cd ../project_2
$ touch __init__.py
$ touch people.py

$ cd ../docs
$ touch factorial.rst
$ touch people.rst
$ vi conf.py
$ vi index.rst
$ make html
$ open _build/html/index.html 
$ cd ..
$ git status
$ git add .
$ git commit -am "with link to modules documentation"
$ git push origin master


$ make html
