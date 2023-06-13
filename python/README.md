# Python

[Python.org](https://www.python.org)

### Learning

- [Learn Python the Hard Way](https://learncodethehardway.org/python/)
- [Codecademy: Python Courses & Tutorials](https://www.codecademy.com/catalog/language/python)
- [Google's Python Class](https://developers.google.com/edu/python/)
- [Interviewbit: Python Course](https://www.interviewbit.com/blog/best-free-python-course/)

### Conferences

- [PyCon](https://us.pycon.org/)
    - [YouTube](https://www.youtube.com/c/PyConUS/videos)

## Intro to Python

Notes from [Jaimie Murdock](https://gist.github.com/JaimieMurdock/40fab1ce8fea8d06d3279955a6090548):

Assumes a start with Python 3.6. Python 2.7 is end of life in 2020, so new projects should avoid it.

## Important PEPs

PEPs (Python Enhancement Proposals) are how new features are added to the language and are very useful for learning why things are the way they are.

Some also offer style guidance.

- Coding style
  - [PEP 8  -- Style Guide for Python Code](https://www.python.org/dev/peps/pep-0008/)
  - [PEP 257 -- Docstring Conventions](https://www.python.org/dev/peps/pep-0257/)
- Lists, iterators, and generators
  - [PEP 202 -- List Comprehensions](https://www.python.org/dev/peps/pep-0202/)
  - [PEP 275 -- Dict Comprehensions](https://www.python.org/dev/peps/pep-0274/)
  - [PEP 234 -- Iterators](https://www.python.org/dev/peps/pep-0234/)
  - [PEP 255 -- Simple Generators](https://www.python.org/dev/peps/pep-0255/)
  - [PEP 289 -- Generator Expressions](https://www.python.org/dev/peps/pep-0289/) -- most of the time a list comprehension can be done as a generator when passed as an argument, as long as the calling function doesn't need the `len()` of the list. This improves memory usage.
  - [PEP 279 -- The enmerate() built-in function](https://www.python.org/dev/peps/pep-0279/)
- Syntax
  - [PEP 343 -- The "with" statement](https://www.python.org/dev/peps/pep-0343/) -- really great way to make sure files are closed when done being read.
  - [PEP 498 -- Literal String Interpolation](https://www.python.org/dev/peps/pep-0498/) -- `f`-strings, requires Python 3.6

## Useful modules
- General
  - [`collections`](https://docs.python.org/3/library/collections.html) -- especially `defaultdict`, which helps avoid `KeyError` issues when populating a collection
  - [`pickle`](https://docs.python.org/3/library/pickle.html) -- Python-native serialization. For export, better practice to use JSON via `json.dump(obj)`, but useful when in-memory objects take a long time to build.
  - [`re`](https://docs.python.org/3/library/re.html)
- Script Management  
  - [`argparse`](https://docs.python.org/3/library/argparse.html)
  - [`logging`](https://docs.python.org/3/library/logging.html)
- Web
  - [`json`](https://docs.python.org/3/library/json.html)
  - [`urllib`](https://docs.python.org/3/library/urllib.html)
  - [bottle](http://bottlepy.org/) -- `pip install bottle` -- nanoframework, useful for quick mockups
  - [flask](http://flask.pocoo.org/) -- `pip install flask` -- microframework
- Threading and Process Management
  - [`concurrent.futures`](https://docs.python.org/3/library/concurrent.futures.html)
  - [`subprocess`](https://docs.python.org/3/library/subprocess.html)
- Testing
  - [`unittest`](https://docs.python.org/3/library/unittest.html)
  - [`unittest.mock`](https://docs.python.org/3/library/unittest.mock.html) -- super useful for injecting fake-responses from HTTP servers for testing
  - [`coverage.py`](https://coverage.readthedocs.io/en/coverage-4.4.2/) -- `pip install coverage`

## Useful non-stdlib modules
- [Matplotlib](https://matplotlib.org/)
- [pandas](https://pandas.pydata.org/)
- [scikit-learn](http://scikit-learn.org/stable/)
- [SQLAlchemy](https://www.sqlalchemy.org/)
