# (My) WebAPIs

This is a collection of all my WebAPIs

## Table of Contents
+ [Information](#information)
+ [Files](#files)
+ [Documentation](#documentation)

## Information

This is part of my repository for all my APIs that derived from me needing to refer to some of my manuals and documentations for things like
- FOSS Packages
	- names, urls etc

Thus, I came up with a repository to store all my APIs

This folder is for my WebAPIs (still researching on if I should just categorise these under API, or seperating would be better) in which the idea is
you can see which API is useful for your needs, just import in your web browser, program files, JSON includes etc. and it <b>should</b> work.

At the moment, it is still a WIP and is technically considered in development, thus as such - *Your Mileage may Vary*

If you would like to contribute to the project (Thank you in advance), please refer to my [CONTRIBUTING.md]("../CONTRIBUTING.md")

## Files
+ [foss_pkgs.json](foss_pkgs.json) : This API contains (or indeed, aims to contain) as many FOSS package information such as links, package names, methods etc. for programming usage

## Documentation

### Synopsis/Syntax

- JSON file format
	- Import in HTML
		```html
		<script type="text/javascript" src="https://raw.githubusercontent.com/Thanatisia/"> </script>
		```

	- Import in Python
		- via REST (remote) API
			- using urllib.request
				```python
				import urllib.request as request

				res = request.get("https://link/to/file.json")
				contents = res.decode(res)
				```
			- using requests
				```python
				import requests

				res = requests.get("https://link/to/file.json")
				```


### Parameters

### Usage