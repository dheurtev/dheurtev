# My picks for Python tools and packages

- [Introduction - when to use Python](#introduction---when-to-use-python)
- [Implementations](#implementations)
- [Distributions](#distributions)
- [Development tool chain : scaffold, coding style checkers, test, documentation, repository](#development-tool-chain--scaffold-coding-style-checkers-test-documentation-repository)
- [Virtual Environment, Package installers](#virtual-environment-package-installers)
- [Data Science Libraries](#data-science-libraries)
- [Machine Learning Libraries](#machine-learning-libraries)
- [Data vizualization](#data-vizualization)
- [Natural Language Processing](#natural-language-processing)
- [Image processing](#image-processing)
- [ETL Tools](#etl-tools)
- [Data : ORM, Validation](#data--orm-validation)
- [Web](#web)
- [Other tools](#other-tools)

## Introduction - when to use Python ##
**[`^        back to top        ^`](#)**
- Python is an interpreted scripting language 
- It is great to act as a glue with modules in other languages (C, C++).
- It is slow if the code is written in pure Python (>x100 times C). PyPy can make it faster (approximately x5).
- [Beware of GIL = single thread - Real Python](https://realpython.com/python-gil/)
- Suitable for :
  * Automation - A replacement of bash scripts in sysadmin tasks
  * Computer security
  * Data science (with optimized data science libraries)
  * AI
  * APIs
  * Small hobby projects
- Consider alternatives for :
  * CLI : Rust
  * Web apps: Javascript, PHP
  * API, Microservices : ASP.NET core, Spring Boot, express.js, GO
  * Native android/iOS apps: Swift, Java, Kotlin
  * Cross-platform mobile apps: flutter
  * Desktop GUI: C#, C++, Pascal/Delphi (RAD)

## Implementations ##
**[`^        back to top        ^`](#)**
- [Python - CPython](https://www.python.org/): high-level, interpreted, general-purpose programming language. Cross-platform. Python Software Licence. [in use]
- [PyPy](https://www.pypy.org/): ternative implementation of the Python programming language to CPython. PyPy often runs faster than CPython because PyPy uses a just-in-time compiler. MIT License.

## Distributions ##
**[`^        back to top        ^`](#)**
- [Anaconda](https://anaconda.org/): distribution of the Python and R programming languages for scientific computing, that aims to simplify package management and deployment. Windows, Linux, Mac. Freemium. [in use]
- [Miniconda](https://docs.conda.io/en/latest/miniconda.html): Free minimal installer for conda. It is a small, bootstrap version of Anaconda that includes only conda, Python, the packages they depend on, and a small number of other useful packages, including pip, zlib and a few others. Has access to conda. [in use]

## Development tool chain : scaffold, coding style checkers, test, documentation, repository ##
**[`^        back to top        ^`](#)**
[Packaging Python Projects - Official](https://packaging.python.org/en/latest/tutorials/packaging-projects/)
[How to publish a package on PyPi - Real Python](https://realpython.com/pypi-publish-python-package/)
[Python package lesson](https://github.com/BillMills/pythonPackageLesson)
[ReadTheDocs Tutorial](https://docs.readthedocs.io/en/stable/tutorial/)
### Package Scaffold ###
- [PyScaffold](https://pypi.org/project/PyScaffold/): Python project scaffold. MIT License [in use]
### Coding style Checkers ###
- [Flake8](https://github.com/pycqa/flake8): modular source code checker: pep8 pyflakes and co. MIT License [in use] 
- [black](https://github.com/psf/black). uncompromising code formatter. MIT License [in use]
## Test ##
- [PyTest](https://docs.pytest.org/en/7.1.x/): Python testing framework. MIT License. [in use]
- [Python Selenium bindings](https://selenium-python.readthedocs.io/) [past]
### Documentation ###
- [Sphinx](https://www.sphinx-doc.org/en/master/): Python Documentation generator. BSD 2-Clause "Simplified" License [in use]
- [myst-parser](https://pypi.org/project/myst-parser/): An extended commonmark compliant parser, with bridges to docutils & sphinx.  [in use] 
- [docutils](https://pypi.org/project/docutils/): Python Documentation Utilities. Public License. [in use]
### Repository ###
- [PyPi](https://pypi.org/): repository of software for the Python programming language. [in use]

## Virtual Environment, Package installers ##
**[`^        back to top        ^`](#)**
[Virtual Environment Primer - Real Python](https://realpython.com/python-virtual-environments-a-primer/)
- conda (see Anaconda or Miniconda)
- [pip](https://pypi.org/project/pip/): package installer for Python. MIT License. [in use]
- [pipx](https://pypa.github.io/pipx/): Install and Run Python Applications in Isolated Environments.  It creates a virtual environment for each tool and makes it globally accessible. Similar to brew or npx. MIT License. [in use]
- [venv](https://docs.python.org/3/library/venv.html): Creation of virtual environments. PSF License. [in use]
- [virtualenv](https://virtualenv.pypa.io/en/latest/): create isolated Python environments. Since Python 3.3 , a subset of it has been integrated into the standard library under the venv module. MIT License. [in use]
- [pyenv](https://github.com/pyenv/pyenv): Install and manage several python versions. MIT License. [in use]
- [SetupTools](https://github.com/pypa/setuptools): Download, build, install, upgrade, and uninstall Python packages. [in use]  
- [Tox](https://tox.readthedocs.io/): generic virtualenv management and test command line tool. MIT License [in use]

## Data Science Libraries ##
**[`^        back to top        ^`](#)**
- [IPython](https://ipython.org/): command shell for interactive computing in multiple programming languages. BSD License [in use]
- [Jupyter](https://jupyter.org/): web-based interactive computing platform. modified BSD license. [in use]
- [Pandas](https://pandas.pydata.org/): software library written for the Python programming language for data manipulation and analysis. New BSD License. [past]
- [NumPy](https://numpy.org/): library for the Python programming language, adding support for large, multi-dimensional arrays and matrices, along with a large collection of high-level mathematical functions to operate on these arrays. BSD. [past]
- [SciPy](https://scipy.org/): free and open-source Python library used for scientific computing and technical computing. BSD-new license. [past]
- [Numba](https://numba.pydata.org/): open-source JIT compiler that translates a subset of Python and NumPy into fast machine code using LLVM, via the llvmlite Python package
- [StatsModels](https://www.statsmodels.org/stable/index.html): Python package that allows users to explore data, estimate statistical models, and perform statistical tests. Modified BSD (3-clause) license
### References ###
- [NumPy vs. NumPy+Numba](https://dataconomy.com/2017/07/big-data-numpy-numba-python/)
- [Numba for data science](https://www.analyticsvidhya.com/blog/2021/04/numba-for-data-science-make-your-py-code-run-1000x-faster/)
- [Numba + Pandas](https://coderzcolumn.com/tutorials/python/guide-to-speed-up-code-involving-pandas-dataframe-using-numba)

## Machine Learning Libraries ##
**[`^        back to top        ^`](#)**
- [Tensor Flow](https://www.tensorflow.org/): Machine Learning. Apache 2.0 License.
- [Scikit-Learn](https://scikit-learn.org/stable/): Unsupervised learning algorithms. Feature extraction. It features various classification, regression and clustering algorithms including support-vector machines, random forests, gradient boosting, k-means and DBSCAN, and is designed to interoperate with the Python numerical and scientific libraries NumPy and SciP. New BSD License
- [PyTorch](https://pytorch.org/): computer vision and natural language processing. BSD License.
- [Keras](https://keras.io/): artificial neural networks. Keras acts as an interface for the TensorFlow library. Apache 2.0
- [LightGBM](https://lightgbm.readthedocs.io/en/v3.3.2/): redefined elementary models and namely decision trees. MIT License

## Data vizualization ##
**[`^        back to top        ^`](#)**
[Data visualization libraries](https://mode.com/blog/python-data-visualization-libraries/)
- [Matplotlib](https://matplotlib.org/): plotting library for the Python programming language and its numerical mathematics extension NumPy. [in use] 
- [Seaborn](https://seaborn.pydata.org/): Python data visualization library based on matplotlib.

## Natural Language Processing ##
**[`^        back to top        ^`](#)**
- [NLTK](https://www.nltk.org/): suite of libraries and programs for symbolic and statistical natural language processing for English. Apache 2.0 License.

## Image processing ###
**[`^        back to top        ^`](#)**
- [Pillow](https://pillow.readthedocs.io/en/stable/): free and open-source additional library for the Python programming language that adds support for opening, manipulating, and saving many different image file formats

## ETL Tools ##
**[`^        back to top        ^`](#)**
- [Bonobo](https://www.bonobo-project.org/) : Data pipelines. lightweight Extract-Transform-Load (ETL) framework for Python 3.5+ [considering]
- [Mara]](https://github.com/mara) : Halfway between scripts and complex solutions like Airflow [considering]

## Data : ORM, Validation ##
**[`^        back to top        ^`](#)**
- [SQLAlchemy](https://sqlalchemy.org/): Database toolkit, Object Relationship Mapper. Compatible with Flask and Pyramid [in use]
- [Pydantic](https://pydantic-docs.helpmanual.io/):Data validation and settings management using python type annotations. MIT License.

## Web ##
**[`^        back to top        ^`](#)**
### HTTP Library ###
- [urllib3](https://urllib3.readthedocs.io/): powerful, user-friendly HTTP client for Python. MIT License [in use]
- [Requests](https://pypi.org/project/requests/): HTTP library for the Python programming language. Apache 2.0 License. [in use]
- [HTTPX](https://www.python-httpx.org/): fully featured HTTP client for Python 3, which provides sync and async APIs, and support for both HTTP/1.1 and HTTP/2. BSD License.
### HTML / XML Parser ###
- [Beautiful Soup](https://www.crummy.com/software/BeautifulSoup/bs4/doc/): Python package for parsing HTML and XML documents. MIT License 4 [in past]
### Scrapper / Spiders / Web crawlers ###
- [Scrapy](https://scrapy.org/): Free and open-source web-crawling framework written in Python. Originally designed for web scraping, it can also be used to extract data using APIs or as a general-purpose web crawler. BSD License. [in past]
### Web Frameworks ###
[Comparison](https://codeahoy.com/compare/python-frameworks)
[Official list](https://wiki.python.org/moin/WebFrameworks)
#### Full stack ####
- [Django](https://www.djangoproject.com/): high-level Python web framework follows the model–views–template (MVT) architectural pattern. BSD 3 license. Great for database oriented models [past]
- [Web2Py](https://www.web2py.com/): All in one package with no further dependencies. Development, deployment, debugging, testing, database administration and maintenance of applications can be done via the provided web interface, but not required. LGPLv3. [past] 
- [Pyramid](https://trypyramid.com/): high-level Python web framework. Integrates with Jinja2 and SQL Alchemy. BSD-derived Repoze Public License [past : Not recommended on new projects] 
#### Micro ####
- [Flask](https://flask.palletsprojects.com/en/2.2.x/): micro web framework written. Does not require particular tools or libraries. No database abstraction layer, form validation, or any other components where pre-existing third-party libraries provide common functions. Not async friendly [in use, recommended for sync small projects]
  * [Flask front end example - Real Python](https://realpython.com/the-ultimate-flask-front-end/)
- [Bottle](https://bottlepy.org/docs/dev/) Fast and simple micro-framework for small web-applications. It offers request dispatching (Routes) with url parameter support, Templates, key/value Databases, a build-in HTTP Server and adapters for many third party WSGI/HTTP-server and template engines. All in a single file and with no dependencies other than the Python Standard Library. MIT License [in use, not recommended on new projects use FastAPI]
  * [Documentation](https://bottle-rest.readthedocs.io/en/latest/)
  * [API Building example - topal](https://www.toptal.com/bottle/building-a-rest-api-with-bottle-framework)
  * [Rest API Example - simplifiedpython](https://www.simplifiedpython.net/python-rest-api-example/)
#### API ####
- [FastAPI](https://fastapi.tiangolo.com/) Web framework for developing RESTful APIs in Python. FastAPI is based on Pydantic and type hints to validate, serialize, and deserialize data, and automatically auto-generate OpenAPI documents. It fully supports asynchronous programming and can run with Uvicorn and Gunicorn. MIT License.
  * [FastAPI example - Real Python](https://realpython.com/fastapi-python-web-apis/)
  * [FastAPI bloilerplate](https://github.com/teamhide/fastapi-boilerplate)

#### Other web tools ####
- [Jinja2](https://jinja.palletsprojects.com/en/3.1.x/): web template engine for the Python programming language. BSD License [in use]
- [Starlete](https://www.starlette.io/): Async Web services Lightweight ASGI framework/toolkit. WebSocket support. BSD License.
- [Celery](https://docs.celeryq.dev/en/stable/getting-started/introduction.html): Long tasks / Queues (celerybeat - scheduler, celeryd - daemon). Real time. Scheduling supported. BSD License.
- [pyjwt](https://pyjwt.readthedocs.io/en/stable/): Python library which allows you to encode and decode JSON Web Tokens (JWT). MIT License.
- [Authlib](https://docs.authlib.org/en/latest/): ultimate Python library in building OAuth and OpenID Connect servers. BSD 3 License
- [Boto3](https://github.com/boto/boto3): AWS SDK for Python. Apache 2.0 License.
- [Certifi](https://github.com/certifi/python-certifi): A carefully curated collection of Root Certificates for validating the trustworthiness of SSL certificates while verifying the identity of TLS hosts. Mozilla Public License, v. 2.0.

#### Best Django packages ####
https://blog.devgenius.io/2021-top-100-django-packages-list-during-the-year-92fef0ba79c9
https://viewflow.medium.com/top-102-most-downloaded-django-packages-in-2020-108f0cd372e7
- django-rest-framework
- django-filter-queryset
- django-storage
- django-debug-toolbar
- django-rest-auth
- django-rest-swagger
- django-restframework-jwt
- django-oauth-toolkit
- django-cors-headers
- pytest-django
- django-celetry
- django-celery-beat
- django-all-auth
- wagtail
- social-auth-app-django

## Other tools ##
**[`^        back to top        ^`](#)**
- [Click](https://click.palletsprojects.com/en/8.1.x/): Beautiful command line interfaces in a composable way with as little code as necessary. BSD License (BSD-3-Clause) [in use]
- [Six](https://github.com/benjaminp/six): Python 2 and 3 compatibility utilities. MIT License
- [PyYAML](https://pyyaml.org/): YAML parser and emitter for Python [in use]
- [typing-extensions](https://pypi.org/project/typing-extensions/): Backported and Experimental Type Hints for Python 3.7+. PSF License.
- [Distro](https://github.com/python-distro/distro): OS platform information API [in use]
