# Apama event parser
[![Build Status](https://travis-ci.org/DanskeBank/apamaeventparser.svg?branch=master)](https://travis-ci.org/DanskeBank/apamaeventparser)
[![Coverage Status](https://coveralls.io/repos/github/DanskeBank/apamaeventparser/badge.svg?branch=master)](https://coveralls.io/github/DanskeBank/apamaeventparser?branch=master)
[![PyPI version](https://badge.fury.io/py/apamaeventparser.svg)](https://badge.fury.io/py/apamaeventparser)
## Description

A parser for Apama epl events. 
[Apama](http://www.softwareag.com/corporate/products/apama_webmethods/analytics/overview/default.asp) 
is a complex event processor that uses a domain specific language for working with the event engine.
Testing is done using some apama specific extensions to [pysys](https://sourceforge.net/projects/pysys/).

This project provides a parser for apama events, with the intention to be used with the testing framework.

## How to use

Pass an event as a string to the parse method in eventparser.py. The result is an ApamaEvent
object. The ApamaEvent definition can be found in apamaevent.py

```
from apamaeventparser.eventparser import parse
event = parse('com.apama.Event("Field", 1.234, 7, false, ["a","b","c"], {"key": "value"})')
```

An event can be created from the ApamaEvent object using the unparse method.

## Dependencies
See requirements.txt
