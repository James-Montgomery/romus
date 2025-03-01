# Romus

Romus is a passion project of mine. I often have to deal with coding up simple conjugate models and gibbs samplers at work. This is useful for the variety of experimentation asks my data science team supports. I also use these models to help educate more junior data scientists about Bayesian statistics. This package is meant to serve a dual purpose as a tool for simple modeling and as an example for educational purposes.

I'm open to all questions, feedback, commentary, and suggestions as long as they are constructive and polite! Discussions should always come in the form of git issues.

### Authors

**James Montgomery** - *Initial Work* - [jamesmontgomery.us](http://jamesmontgomery.us)

### License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## About the Name

Why call the package Romus? Romulus and Remus were a famous pair of twins whose myth is tied to the founding of Rome. Conjugate distributions (or distributions closed under sampling) are pairs of distributions who have a special relationship that is sometimes useful in machine learning and statistics. Therefore I thought it would be fun to name my package after a famous pair of twins!

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Installing

For a local installation, first git clone this repository. Then follow these instructions:

```
pip install .
```

To install from [pypi](#):

```
pip install -U romus
```

## Testing

Testing is an important part of creating maintainable, production grade code. Below are instructions for running unit and style tests as well as installing the necessary testing packages. Tests have intentionally been separated from the installable pypi package for a variety of reasons.

Make sure you have the required testing packages:

```
pip install -r requirements_test.txt
```

### Running the unit tests

We use the pytest framework for unit testing.

```
pytest -vvl -s --cov romus --disable-pytest-warnings
```

### Running the style tests

Having neat and legible code is important. Having documentation is also important. We use pylint as our style guide framework. Many of our naming conventions follow directly from the literary sources they come from. This makes it easier to read the mathematical equations and see how they translate into the code. This sometimes forces us to break pep8 conventions for naming.

```
pylint romus --disable=invalid-name
```

## Contributor's Guide

Here are some basic guidelines for contributing.

### Branch Strategy

This repository doesn't use a complicated branching strategy. Simply create a feature branch off of master. When the feature is ready to be integrated with master, submit a pull request. A pull request will re quire at least one peer review and approval from the repository owner.

### Style Guide

Please stick to pep8 standards when for your code. Use numpy style docstrings.

### Test Requirements

Please use pytest as your testing suite. You code should have >= 80% coverage.

### Updating the Docs

<!--
sphinx-quickstart --ext-autodoc
# comment conf.py file
# add docs/.nojekyll file
# update build dir in docs/Makefile
# update static dir in docs/conf.py
# create dummy docs/index.html
-->

Updating the documentation is simple. First, let auto-docs check for updates to the package structure.

```
cd docs
sphinx-apidoc -o . ../romus/
```

Finally, rebuild the html files.

```
make html
```

## Acknowledgments

A big thank you to Keegan Hines and Mack Sweeney both of who helped start me on my journey into Bayesian statistics.

## TODO

This package is still in the development phase. Here I list some tasks that are still left to be completed...

* Add ToC to README
* Add gibbs samplers to package
* Add mixture conjugate models to package
* Fill out examples
* Fill out model specification docs
* Fill out distributions docs
* Update docstrings
  * module docstrings
  * class docstrings
  * function docstrings
* Type Hints
* Proper Test
  * Units Tests
  * Smoke Tests
  * Integration Tests
* Add docs
* Add branch protection

## Useful Resources

### General

* [Wikipedia](https://en.wikipedia.org/wiki/Conjugate_prior)
* [Conjugate Compedndium](https://www.johndcook.com/CompendiumOfConjugatePriors.pdf)
* [MAS3301 Bayesian Statistics W4](http://www.mas.ncl.ac.uk/~nmf16/teaching/mas3301/week4.pdf)
* [MAS3301 Bayesian Statistics W5](http://www.mas.ncl.ac.uk/~nmf16/teaching/mas3301/week5.pdf)
* [MIT18-05S14 Reading15a](https://ocw.mit.edu/courses/mathematics/18-05-introduction-to-probability-and-statistics-spring-2014/readings/MIT18_05S14_Reading15a.pdf)
* [Conjugate families of distributions](http://halweb.uc3m.es/esp/Personal/personas/mwiper/docencia/English/PhD_Bayesian_Statistics/ch3_2009.pdf)

### Distribution Specific

* [The Conjugate Prior for the Normal Distribution](https://people.eecs.berkeley.edu/~jordan/courses/260-spring10/lectures/lecture5.pdf)
* [Conjugate Bayesian analysis of the Gaussian distribution](https://www.cs.ubc.ca/~murphyk/Papers/bayesGauss.pdf)
* [Notes on the Negative Binomial Distribution](https://www.johndcook.com/negative_binomial.pdf)
* [Beta-Binomial vs Hypergeometric](https://stats.stackexchange.com/questions/311088/beta-binomial-as-conjugate-to-hypergeometric)
