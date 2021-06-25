Pandas cookbook
===============

[![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/jvns/pandas-cookbook/master)

[pandas](http://pandas.pydata.org/) is a Python library for doing
data analysis. It's really fast and lets you do exploratory work
incredibly quickly.

The goal of this cookbook is to give you some concrete examples for
getting started with pandas. The [docs](http://pandas.pydata.org/pandas-docs/stable/)
are really comprehensive. However, I've often had people
tell me that they have some trouble getting started, so these are
examples with real-world data, and all the bugs and weirdness
that entails.

It uses 3 datasets:

* 311 calls in New York
* How many people were on Montréal's bike paths in 2012
* Montreal's weather for 2012, hourly

It comes with batteries (data) included, so you can try out all the
examples right away.

Table of Contents
=================


* A quick tour of the IPython Notebook
  <br> Shows off IPython's awesome tab completion and magic functions.
* Chapter 1: Reading from a CSV
  <br> Reading your data into pandas is pretty much the easiest thing. Even when the encoding is wrong!
* Chapter 2: Selecting data & finding the most common complaint type
  <br>It's not totally obvious how to select data from a pandas dataframe. Here I explain the basics (how to take slices and get columns)
* Chapter 3: Which borough has the most noise complaints? (or, more selecting data)
  <br>Here we get into serious slicing and dicing and learn how to filter dataframes in complicated ways, really fast.
* Chapter 4: Find out on which weekday people bike the most with groupby and aggregate
  <br> The groupby/aggregate is seriously my favorite thing about pandas and I use it all the time. You should probably read this.
* Chapter 5: Combining dataframes and scraping Canadian weather data
  <br>Here you get to find out if it's cold in Montreal in the winter (spoiler: yes). Web scraping with pandas is fun!
* Chapter 6: String operations! Which month was the snowiest?
  <br> Strings with pandas are great. It has all these vectorized string operations and they're the best. We will turn a bunch of strings containing "Snow" into vectors of numbers in a trice.
* Chapter 7: Cleaning up messy data
  <br> Cleaning up messy data is never a joy, but with pandas it's easier &lt;3
* Chapter 8: Parsing Unix timestamps
  <br> This is basically a quick trick that took me 2 days to figure out.
* Chapter 9 - Loading data from SQL databases
  <br> How to load data from an SQL database into Pandas, with examples using SQLite3, PostgreSQL, and MySQL.

How to use this cookbook
========================

The easiest way is to try it out instantly online using Binder's awesome service. **[Start by clicking here](https://mybinder.org/v2/gh/jvns/pandas-cookbook/master)**, wait for it to launch, then click on "cookbook", and you'll be off to the races! It will let you run all the code interactively without having to install anything on your computer.

To install it locally , you'll need an up-to-date version of IPython Notebook (&gt;= 3.0) and
n your computer
pandas (&gt;=0.13) for this to work properly. It's set up to work with Python 2.7.

You can get these using `pip` (you may want to do this inside a virtual environment to avoid conflicting with your other libraries).

```bash
  pip install -r requirements.txt
```

This can be difficult to get set up and require you to compile
a whole bunch of things. I instead use and recommend
[Anaconda](https://store.continuum.io/), which is a Python distribution which
will give you everything you need. It's free and open source.

Once you have pandas and IPython, you can get going!

```bash
git clone https://github.com/jvns/pandas-cookbook.git
cd pandas-cookbook/cookbook
ipython notebook
```

A tab should open up in your browser at `http://localhost:8888`

Happy pandas!

Running the cookbook inside Docker container.
===============================================================
This repository contains Dockerfile and can be built into a docker container.
To build the container run following command from inside of the repository directory:
```
docker build -t jvns/pandas-cookbook -f Dockerfile-Local .
```
run the container:
```
docker run -d -p 8888:8888 -e "PASSWORD=MakeAPassword" <IMAGE ID>
```
you can find out about the id of the image, by checking
```
docker images
```

After starting the container, you can access ipython notebook with the cookbook
on port 8888. Remember to use https and authenticate with `MakeAPassword`.
```
https://<docker ip>:8888
```


License
=======

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="http://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />

This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/)

## Translations

There's [a translation into Chinese of this repo](https://github.com/ia-cas/pandas-cookbook).
