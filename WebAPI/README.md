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

- [JSON API](json)
    + [foss_pkgs.json](foss_pkgs.json) : This API contains (or indeed, aims to contain) as many FOSS package information such as links, package names, methods etc. for programming usage

## Documentation

### Synopsis/Syntax

- JSON file format
	- Import in HTML/CSS3/Javascript
        - Using pure javascript via XMLHttpRequest (Static Website supported, Recommended to use AJAX)
            ```javascript
            /*
            Thanks to the following references for this advice
            - https://stackoverflow.com/questions/2499567/how-to-make-a-json-call-to-an-url/2499647#2499647 : Importing JSON using purely GET request
            */
            
            const xmlhttp = new XMLHttpRequest();
            var json_api_url = "https://raw.githubusercontent.com/Thanatisia/api/main/WebAPI/api_name_here.json";
            
            // HTTP GET request 
            var HTTPreq = new XMLHttpRequest();                 // Create new XML HTTP Request
            HTTPreq.open("GET", json_api_url, false);           // Open GET request and download from URL
            HTTPreq.send(null);                                 // Send back nothing to complete the TCP/IP Handshake (SYN, ACK-SYN, SYN)
            var http_res_content = HTTPreq.responseText;        // Get the response text from the GET request packet
            
            // Read in GET response text and parse into JSON
            var json_content = JSON.parse(http_res_content);    // Parse GET response string into JSON 
            
            // Use JSON object
            var value = json_content.key_name;
            console.log(value + " : " + "key_name");
            ```
            
        - Using FetchAPI (Dynamic Website)
            - Dependencies
                - Server
                    + Node.JS
                + JQuery
            - Code
                ```javascript
                <script src="javascript">
                    fetch('https://raw.githubusercontent.com/Thanatisia/api/main/WebAPI/api_name_here.json')
                        .then(res => res.json())
                        .then( (out) => {
                            console.log('Output: ', out);
                        }).catch(err => console.error(err));
                </script>
                ```
        
        - Using AJAX with FetchAPI (Dynamic Website)
            - Dependencies
                - Server
                    + Node.JS
                    + Apache
                + AJAX
                + JQuery
            - Code
                ```javascript
                
                // Get FETCH response from URL
                json_api_url = "https://raw.githubusercontent.com/Thanatisia/api/main/WebAPI/api_name_here.json";
                
                // Asynchronous function to get URL and the response
                const getJSON = async url => {
                    // Get FETCH response
                    const response = await fetch(url);
                    
                    // Error Checking
                    if(response.ok) // Check if response worked (no 404 errors etc)
                    {
                        var data = response.json(); // Get JSON from response 
                    }
                    
                    // Return output
                    return data;
                }
                
                // Use function
                getJSON(json_api_url)
                    .then(data => {
                        // Statements
                        console.log(data);
                    }).catch(error => {
                        // Error Statements
                        console.error(error);
                    });
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
