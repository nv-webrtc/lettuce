![Lettuce](./docs/lettuce.png)

# Lettuce, Mobile Framework

[![Build Status](https://api.travis-ci.org/phodal/lettuce.png)](https://travis-ci.org/phodal/lettuce)
[![Version](http://img.shields.io/npm/v/lettuce.svg)](http://http://img.shields.io/npm/v/lettuce.svg)
[![Code Climate](https://codeclimate.com/github/phodal/lettuce/badges/gpa.svg)](https://codeclimate.com/github/phodal/lettuce)
[![Test Coverage](https://codeclimate.com/github/phodal/lettuce/badges/coverage.svg)](https://codeclimate.com/github/phodal/lettuce)

Lettuce is a Small & Powerful Framework for Romantic.
Online demo [http://phodal.github.io/lettuce](http://phodal.github.io/lettuce/#/).

##Example

1.new a instance

```javascript
var L = new lettuce();
```
2.define data

```javascript
var data = {
    about: "Template",
    what: "This about A Mobile Framework For Romantic",
    why: "Why is a new Framework"
};
```

3.create function for router

```javascript
function about() {
    var result = L.tmpl("<h3>{%=o.about%}</h3>", data);
    document.getElementById("results").innerHTML = result;
};

function what() {
    var result = L.tmpl("<h3>{%=o.what%}</h3>", data);
    document.getElementById("results").innerHTML = result;
}

function why() {
    var result = L.tmpl("<h3>{%=o.why%}</h3>", data);
    document.getElementById("results").innerHTML = result;
}
```
4.Add router

```javascript
L.Router
    .add(/#about/, about)
    .add(/#what/, what)
    .add(/#why/, why)
    .load();
```

##Process

###Done

- Template
- Router
- Ajax
- Class
- Promise
- Event

###On Going

- Model

##Simple View


```javascript
var pageView = function(){};
pageView.prototype = {
    init:function(){
        var result = L.tmpl("<h3>" + this.message + "</h3>", data);
        document.getElementById("results").innerHTML = result;
    }
};

var about = new L.Class(pageView);
about.prototype.message = data.about;

var what = new L.Class(pageView);
what.prototype.message = data.what;

var why = new L.Class(pageView);
why.prototype.message = data.why;
```



## License

© 2015 [Phodal Huang](http://www.phodal.com). This code is distributed under the MIT license. See `LICENSE.txt` in this directory.

[待我代码编成，娶你为妻可好](http://www.xuntayizhan.com/person/ji-ke-ai-qing-zhi-er-shi-dai-wo-dai-ma-bian-cheng-qu-ni-wei-qi-ke-hao-wan/)
