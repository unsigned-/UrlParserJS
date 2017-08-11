# UrlParser

Url parser for javascript, returns an object with all the relevant parts of the url. Returns null on failure.

* Only 2.5kb minified
* No dependencies
* Works without jQuery
* Simple and easy to use

## Getting Started

Download and add `UrlParser` to your project.

```html
<script src="/scripts/UrlParser.min.js" type="text/javascript"></script>
```

## Examples

Parse a url.

```javascript
var _urlParts = UrlParser.parse('https://github.com/pudge330/UrlParserJS');

//--parts object
//  {
//    url: 'https://github.com/pudge330/UrlParserJS'
//    ,scheme: 'https'
//    ,username: ''
//    ,password: ''
//    ,subdomain: ''
//    ,domain: 'github.com'
//    ,host: 'github.com'
//    ,port: ''
//    ,path: '/pudge330/UrlParserJS'
//    ,query: ''
//    ,fragment: ''
//    ,queryString: '/pudge330/UrlParserJS'
//    ,pathParts: [
//      'pudge330'
//      ,'UrlParserJS'
//    ]
//    ,queryVariables: ''
//  }

var _urlParts2 = UrlParser.parse('https://downloads.examplewebsite.com/pudge330/UrlParserJS?type=zip');

//--parts object
//  {
//    url: 'https://downloads.examplewebsite.com/pudge330/UrlParserJS?type=zip'
//    ,scheme: 'https'
//    ,username: ''
//    ,password: ''
//    ,subdomain: 'downloads'
//    ,domain: 'examplewebsite.com'
//    ,host: 'downloads.examplewebsite.com'
//    ,port: ''
//    ,path: '/pudge330/UrlParserJS'
//    ,query: 'type=zip'
//    ,fragment: ''
//    ,queryString: '/pudge330/UrlParserJS?type=zip'
//    ,pathParts: [
//      'pudge330'
//      ,'UrlParserJS'
//    ]
//    ,queryVariables: [
//      type: 'zip'
//    ]
//  }
```

Build a url from a object returned by `parse`.

```javascript
var _url = UrlParser.parse(_urlParts);

//--url
//--https://github.com/pudge330/UrlParserJS

var _url = UrlParser.parse(_urlParts2);

//--url
//--https://downloads.examplewebsite.com/pudge330/UrlParserJS?type=zip
```

## Functions