# api documentation for  [dot (v1.1.1)](http://github.com/olado/doT)  [![npm package](https://img.shields.io/npm/v/npmdoc-dot.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-dot) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-dot.svg)](https://travis-ci.org/npmdoc/node-npmdoc-dot)
#### Concise and fast javascript templating compatible with nodejs and other javascript environments

[![NPM](https://nodei.co/npm/dot.png?downloads=true)](https://www.npmjs.com/package/dot)

[![apidoc](https://npmdoc.github.io/node-npmdoc-dot/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-dot_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-dot/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-dot/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-dot/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Laura Doktorova",
        "email": "ldoktorova@gmail.com"
    },
    "bin": {
        "dottojs": "./bin/dot-packer"
    },
    "bugs": {
        "url": "https://github.com/olado/doT/issues"
    },
    "dependencies": {},
    "description": "Concise and fast javascript templating compatible with nodejs and other javascript environments",
    "devDependencies": {
        "commander": "*",
        "coveralls": "^2.11.14",
        "eslint": "^3.9.1",
        "if-node-version": "^1.1.0",
        "jshint": "*",
        "mkdirp": "*",
        "mocha": "*",
        "nyc": "^8.3.2",
        "pre-commit": "^1.1.3",
        "uglify-js": "*"
    },
    "directories": {},
    "dist": {
        "shasum": "1aa26a12b38b1dcccb496714a44303b72efd9ac0",
        "tarball": "https://registry.npmjs.org/dot/-/dot-1.1.1.tgz"
    },
    "engines": [
        "node >=0.2.6"
    ],
    "gitHead": "90edb5d9e75ed7e26341ff3b4de4dcfc3ee54c4f",
    "homepage": "http://github.com/olado/doT",
    "keywords": [
        "template",
        "fast",
        "simple",
        "templating"
    ],
    "license": "MIT",
    "main": "index",
    "maintainers": [
        {
            "name": "esp",
            "email": "e.poberezkin@me.com"
        },
        {
            "name": "olado",
            "email": "ldoktorova@gmail.com"
        }
    ],
    "name": "dot",
    "nyc": {
        "exclude": [
            "test",
            "node_modules"
        ],
        "reporter": [
            "lcov",
            "text-summary"
        ]
    },
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/olado/doT.git"
    },
    "scripts": {
        "bundle": "uglifyjs doT.js -o doT.min.js -c -m --preamble '/* Laura Doktorova https://github.com/olado/doT */'",
        "eslint": "if-node-version '>=4' eslint *.js --ignore-pattern *.min.js",
        "prepublish": "npm run bundle",
        "test": "npm run eslint && npm run test-cov",
        "test-cov": "nyc mocha test/*.test.js"
    },
    "version": "1.1.1"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module dot](#apidoc.module.dot)
1.  boolean <span class="apidocSignatureSpan">dot.</span>log
1.  [function <span class="apidocSignatureSpan">dot.</span>compile (tmpl, def)](#apidoc.element.dot.compile)
1.  [function <span class="apidocSignatureSpan">dot.</span>encodeHTMLSource (doNotSkipEncoded)](#apidoc.element.dot.encodeHTMLSource)
1.  [function <span class="apidocSignatureSpan">dot.</span>process (options)](#apidoc.element.dot.process)
1.  [function <span class="apidocSignatureSpan">dot.</span>template (tmpl, c, def)](#apidoc.element.dot.template)
1.  object <span class="apidocSignatureSpan">dot.</span>doU
1.  object <span class="apidocSignatureSpan">dot.</span>jslitmus
1.  object <span class="apidocSignatureSpan">dot.</span>templateSettings
1.  string <span class="apidocSignatureSpan">dot.</span>version

#### [module dot.doU](#apidoc.module.dot.doU)
1.  [function <span class="apidocSignatureSpan">dot.doU.</span>template (tmpl, conf)](#apidoc.element.dot.doU.template)
1.  object <span class="apidocSignatureSpan">dot.doU.</span>templateSettings
1.  string <span class="apidocSignatureSpan">dot.doU.</span>version

#### [module dot.jslitmus](#apidoc.module.dot.jslitmus)
1.  [function <span class="apidocSignatureSpan">dot.jslitmus.</span>Test (name, f)](#apidoc.element.dot.jslitmus.Test)
1.  [function <span class="apidocSignatureSpan">dot.jslitmus.</span>clearAll ()](#apidoc.element.dot.jslitmus.clearAll)
1.  [function <span class="apidocSignatureSpan">dot.jslitmus.</span>emit (e)](#apidoc.element.dot.jslitmus.emit)
1.  [function <span class="apidocSignatureSpan">dot.jslitmus.</span>getGoogleChart (normalize)](#apidoc.element.dot.jslitmus.getGoogleChart)
1.  [function <span class="apidocSignatureSpan">dot.jslitmus.</span>on (e, f)](#apidoc.element.dot.jslitmus.on)
1.  [function <span class="apidocSignatureSpan">dot.jslitmus.</span>removeAllListeners (e)](#apidoc.element.dot.jslitmus.removeAllListeners)
1.  [function <span class="apidocSignatureSpan">dot.jslitmus.</span>removeListener (e, f)](#apidoc.element.dot.jslitmus.removeListener)
1.  [function <span class="apidocSignatureSpan">dot.jslitmus.</span>runAll (e)](#apidoc.element.dot.jslitmus.runAll)
1.  [function <span class="apidocSignatureSpan">dot.jslitmus.</span>test (name, f)](#apidoc.element.dot.jslitmus.test)
1.  object <span class="apidocSignatureSpan">dot.jslitmus.</span>platform
1.  object <span class="apidocSignatureSpan">dot.jslitmus.</span>unsupported



# <a name="apidoc.module.dot"></a>[module dot](#apidoc.module.dot)

#### <a name="apidoc.element.dot.compile"></a>[function <span class="apidocSignatureSpan">dot.</span>compile (tmpl, def)](#apidoc.element.dot.compile)
- description and source-code
```javascript
compile = function (tmpl, def) {
		return doT.template(tmpl, null, def);
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dot.encodeHTMLSource"></a>[function <span class="apidocSignatureSpan">dot.</span>encodeHTMLSource (doNotSkipEncoded)](#apidoc.element.dot.encodeHTMLSource)
- description and source-code
```javascript
encodeHTMLSource = function (doNotSkipEncoded) {
		var encodeHTMLRules = { "&": "&#38;", "<": "&#60;", ">": "&#62;", '"': "&#34;", "'": "&#39;", "/": "&#47;" },
			matchHTML = doNotSkipEncoded ? /[&<>"'\/]/g : /&(?!#?\w+;)|<|>|"|'|\//g;
		return function(code) {
			return code ? code.toString().replace(matchHTML, function(m) {return encodeHTMLRules[m] || m;}) : "";
		};
	}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dot.process"></a>[function <span class="apidocSignatureSpan">dot.</span>process (options)](#apidoc.element.dot.process)
- description and source-code
```javascript
process = function (options) {
	//path, destination, global, rendermodule, templateSettings
	return new InstallDots(options).compileAll();
}
```
- example usage
```shell
...
		<div>{{=param.foo}}</div>
	#}}

	{{#def.macro:myvariable}}

####Node module now supports auto-compilation of dot templates from specified path

	var dots = require("dot").process({ path: "./views"});

This will compile .def, .dot, .jst files found under the specified path.
Details
* It ignores sub-directories.
* Template files can have multiple extensions at the same time.
* Files with .def extension can be included in other files via {{#def.name}}
* Files with .dot extension are compiled into functions with the same name and
...
```

#### <a name="apidoc.element.dot.template"></a>[function <span class="apidocSignatureSpan">dot.</span>template (tmpl, c, def)](#apidoc.element.dot.template)
- description and source-code
```javascript
template = function (tmpl, c, def) {
		c = c || doT.templateSettings;
		var cse = c.append ? startend.append : startend.split, needhtmlencode, sid = 0, indv,
			str  = (c.use || c.define) ? resolveDefs(c, tmpl, def || {}) : tmpl;

		str = ("var out='" + (c.strip ? str.replace(/(^|\r|\n)\t* +| +\t*(\r|\n|$)/g," ")
					.replace(/\r|\n|\t|\/\*[\s\S]*?\*\//g,""): str)
			.replace(/'|\\/g, "\\$&")
			.replace(c.interpolate || skip, function(m, code) {
				return cse.start + unescape(code) + cse.end;
			})
			.replace(c.encode || skip, function(m, code) {
				needhtmlencode = true;
				return cse.startencode + unescape(code) + cse.end;
			})
			.replace(c.conditional || skip, function(m, elsecase, code) {
				return elsecase ?
					(code ? "';}else if(" + unescape(code) + "){out+='" : "';}else{out+='") :
					(code ? "';if(" + unescape(code) + "){out+='" : "';}out+='");
			})
			.replace(c.iterate || skip, function(m, iterate, vname, iname) {
				if (!iterate) return "';} } out+='";
				sid+=1; indv=iname || "i"+sid; iterate=unescape(iterate);
				return "';var arr"+sid+"="+iterate+";if(arr"+sid+"){var "+vname+","+indv+"=-1,l"+sid+"=arr"+sid+".length-1;while("+indv+"<l"+
sid+"){"
					+vname+"=arr"+sid+"["+indv+"+=1];out+='";
			})
			.replace(c.evaluate || skip, function(m, code) {
				return "';" + unescape(code) + "out+='";
			})
			+ "';return out;")
			.replace(/\n/g, "\\n").replace(/\t/g, '\\t').replace(/\r/g, "\\r")
			.replace(/(\s|;|\}|^|\{)out\+='';/g, '$1').replace(/\+''/g, "");
			//.replace(/(\s|;|\}|^|\{)out\+=''\+/g,'$1out+=');

		if (needhtmlencode) {
			if (!c.selfcontained && _globals && !_globals._encodeHTML) _globals._encodeHTML = doT.encodeHTMLSource(c.doNotSkipEncoded);
			str = "var encodeHTML = typeof _encodeHTML !== 'undefined' ? _encodeHTML : ("
				+ doT.encodeHTMLSource.toString() + "(" + (c.doNotSkipEncoded || '') + "));"
				+ str;
		}
		try {
			return new Function(c.varname, str);
		} catch (e) {
			<span class="apidocCodeCommentSpan">/* istanbul ignore else */
</span>			if (typeof console !== "undefined") console.log("Could not create a template function: " + str);
			throw e;
		}
	}
```
- example usage
```shell
...

InstallDots.prototype.compileToFile = function(path, template, def) {
	def = def || {};
	var modulename = path.substring(path.lastIndexOf("/")+1, path.lastIndexOf("."))
		, defs = copy(this.__includes, copy(def))
		, settings = this.__settings || doT.templateSettings
		, compileoptions = copy(settings)
		, defaultcompiled = doT.template(template, settings, defs)
		, exports = []
		, compiled = ""
		, fn;

	for (var property in defs) {
		if (defs[property] !== def[property] && defs[property] !== this.__includes[property]) {
			fn = undefined;
...
```



# <a name="apidoc.module.dot.doU"></a>[module dot.doU](#apidoc.module.dot.doU)

#### <a name="apidoc.element.dot.doU.template"></a>[function <span class="apidocSignatureSpan">dot.doU.</span>template (tmpl, conf)](#apidoc.element.dot.doU.template)
- description and source-code
```javascript
template = function (tmpl, conf) {
		conf = conf || doU.templateSettings;
		var str = '', tb = conf.begin, te = conf.end, m, l,
			arr = tmpl.replace(/\s*<!\[CDATA\[\s*|\s*\]\]>\s*|[\r\n\t]|(\/\*[\s\S]*?\*\/)/g, '')
				.split(tb).join(te +'\x1b')
				.split(te);

		for (m=0,l=arr.length; m < l; m++) {
			str += arr[m].charAt(0) !== '\x1b' ?
			"out+='" + arr[m].replace(/(\\|["'])/g, '\\$1') + "'" : (arr[m].charAt(1) === '=' ?
			';out+=(' + arr[m].substr(2) + ');' : (arr[m].charAt(1) === '!' ?
			';out+=(' + arr[m].substr(2) + ").toString().replace(/&(?!\\w+;)/g, '&#38;').split('<').join('&#60;').split('>').join('&#62;').
split('" + '"' + "').join('&#34;').split(" + '"' + "'" + '"' + ").join('&#39;').split('/').join('&#x2F;');" : ';' + arr[m].substr
(1)));
		}

		str = ('var out="";'+str+';return out;')
			.split("out+='';").join('')
			.split('var out="";out+=').join('var out=');

		try {
			return new Function(conf.varname, str);
		} catch (e) {
			if (typeof console !== 'undefined') console.log("Could not create a template function: " + str);
			throw e;
		}
	}
```
- example usage
```shell
...

InstallDots.prototype.compileToFile = function(path, template, def) {
	def = def || {};
	var modulename = path.substring(path.lastIndexOf("/")+1, path.lastIndexOf("."))
		, defs = copy(this.__includes, copy(def))
		, settings = this.__settings || doT.templateSettings
		, compileoptions = copy(settings)
		, defaultcompiled = doT.template(template, settings, defs)
		, exports = []
		, compiled = ""
		, fn;

	for (var property in defs) {
		if (defs[property] !== def[property] && defs[property] !== this.__includes[property]) {
			fn = undefined;
...
```



# <a name="apidoc.module.dot.jslitmus"></a>[module dot.jslitmus](#apidoc.module.dot.jslitmus)

#### <a name="apidoc.element.dot.jslitmus.Test"></a>[function <span class="apidocSignatureSpan">dot.jslitmus.</span>Test (name, f)](#apidoc.element.dot.jslitmus.Test)
- description and source-code
```javascript
function Test(name, f) {
  var test = this;

  // Test instances get EventEmitter API
  EventEmitter.call(test);

  if (!f) throw new Error('Undefined test function');
  if (!/function[^\(]*\(([^,\)]*)/.test(f)) {
    throw new Error('"' + name + '" test: Invalid test function');
  }

  // If the test function takes an argument, we assume it does the iteration
  // for us
  var isLoop = !!RegExp.$1;

<span class="apidocCodeCommentSpan">  /**
   * Reset test state
   */
</span>  function reset() {
    delete test.count;
    delete test.time;
    delete test.running;
    test.emit('reset', test);
    return test;
  }

  function clone() {
    var test = extend(new Test(name, f), test);
    return test.reset();
  }

  /**
   * Run the test n times, and use the best results
   */
  function bestOf(n) {
    var best = null;
    while (n--) {
      var t = clone();
      t.run(null, true);
      if (!best || t.period < best.period) {
        best = t;
      }
    }
    extend(test, best);
  }

  /**
   * Start running a test.  Default is to run the test asynchronously (via
   * setTimeout).  Can be made synchronous by passing true for 2nd param
   */
  function run(count, synchronous) {
    count = count || test.INIT_COUNT;
    test.running = true;

    if (synchronous) {
      _run(count, synchronous);
    } else {
      setTimeout(function() {
        _run(count);
      }, 1);
    }
    return test;
  }

  /**
   * Run, for real
   */
  function _run(count, noTimeout) {

    try {
      var start, f = test.f, now, i = count;

      // Start the timer
      start = new Date();

      // Run the test code
      test.count = count;
      test.time = 0;
      test.period = 0;

      test.emit('start', test);

      if (isLoop) {
        // Test code does it's own iteration
        f(count);
      } else {
        // Do the iteration ourselves
        while (i--) f();
      }

      // Get time test took (in secs)
      test.time = Math.max(1,new Date() - start)/1000;

      // Store iteration count and per-operation time taken
      test.count = count;
      test.period = test.time/count;

      // Do we need to keep running?
      test.running = test.time < test.MIN_TIME;

      // Publish results
      test.emit('results', test);

      // Set up for another run, if needed
      if (test.running) {
        // Use an iteration count that will (we hope) get us close to the
        // MAX_COUNT time.
        var x = test.MIN_TIME/test.time;
        var pow = Math.pow(2, Math.max(1, Math.ceil(Math.log(x)/Math.log(2))));
        count *= pow;
        if (count > test.MAX_COUNT) {
          throw new Error('Max count exceeded.  If this test uses a looping function, make sure the iteration loop is working properly
.');
        }

        if (noTimeout) {
          _run(count, noTimeout);
        } else {
          run(count);
        }
      } else {
        test.emit('complete', test);
      }
    } catch (err) {
      log(err);
      // Exceptions are caught and displayed in the test UI
      test.emit('error', err);
    }

    return test;
  }

  /**
  * Get the number of operations per second for this test.
  *
  * @param normalize if true, iteration loop overhead taken into account.
  *                  Note that normalized tests may return Infinity if the
  *                  test time is of the same order as the calibration time.
  */
  function getHz(normalize) {
    var p = test.period;

    // Adjust period based on the calibration test time
    if (normalize) {
      var cal = test.isLoop ? Test.LOOP_CAL : Test.NOLOOP_CAL;
      if (!cal.period) {
        // Run calibration if needed
        cal.MIN_TIME = .3;
        cal.bestOf(3);
      }

      // Subtract off calibration time.  In theory this should never be
      // negative, but in practice the calibration times are affected by a
      // variety of factors so just clip to zero and let users test for
      // getHz() == Infinity
      p = Math.max(0, p - cal.period);
    }

    return sig(1/p, 4);
  }

  // Set properties that are specific to this instance
  extend(test, {
    // Test name
    name: name, ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dot.jslitmus.clearAll"></a>[function <span class="apidocSignatureSpan">dot.jslitmus.</span>clearAll ()](#apidoc.element.dot.jslitmus.clearAll)
- description and source-code
```javascript
function clearAll() {
	tests = [];
}
```
- example usage
```shell
...
				for(var i=0; i<3; i++) { snippet += snippet; }
				console.log("*** Large template length: " + snippet.length);
				break;
			default:
				return;
			}

			jslitmus.clearAll();
			testsetup(snippet);
			jslitmus.runAll();
		});
		// Run it!
		jslitmus.runAll();
	}
...
```

#### <a name="apidoc.element.dot.jslitmus.emit"></a>[function <span class="apidocSignatureSpan">dot.jslitmus.</span>emit (e)](#apidoc.element.dot.jslitmus.emit)
- description and source-code
```javascript
emit = function (e) {
  var args = Array.prototype.slice.call(arguments, 1);
  forEach([].concat(listeners[e], listeners['*']), function(l) {
    ee._emitting = e;
    if (l) l.apply(ee, args);
  });
  delete ee._emitting;
}
```
- example usage
```shell
...
/**
 * Reset test state
 */
function reset() {
  delete test.count;
  delete test.time;
  delete test.running;
  test.emit('reset', test);
  return test;
}

function clone() {
  var test = extend(new Test(name, f), test);
  return test.reset();
}
...
```

#### <a name="apidoc.element.dot.jslitmus.getGoogleChart"></a>[function <span class="apidocSignatureSpan">dot.jslitmus.</span>getGoogleChart (normalize)](#apidoc.element.dot.jslitmus.getGoogleChart)
- description and source-code
```javascript
function getGoogleChart(normalize) {
  var chart_title = [
    'Operations/second on ' + platform.name,
    '(' + platform.version + ' / ' + platform.os + ')'
  ];

  var n = tests.length, markers = [], data = [];
  var d, min = 0, max = -1e10;

  // Gather test data

  var markers = map(tests, function(test, i) {
    if (test.count) {
      var hz = test.getHz();
      var v = hz != Infinity ? hz : 0;
      data.push(v);
      var label = test.name + '(' + humanize(hz)+ ')';
      var marker = 't' + escape2(label) + ',000000,0,' + i + ',10';
      max = Math.max(v, max);

      return marker;
    }
  });

  if (markers.length <= 0) return null;

  // Build labels
  var labels = [humanize(min), humanize(max)];

  var w = 250, bw = 15;
  var bs = 5;
  var h = markers.length*(bw + bs) + 30 + chart_title.length*20;

  var params = {
    chtt: escape(chart_title.join('|')),
    chts: '000000,10',
    cht: 'bhg',                     // chart type
    chd: 't:' + data.join(','),     // data set
    chds: min + ',' + max,          // max/min of data
    chxt: 'x',                      // label axes
    chxl: '0:|' + labels.join('|'), // labels
    chsp: '0,1',
    chm: markers.join('|'),         // test names
    chbh: [bw, 0, bs].join(','),    // bar widths
    // chf: 'bg,lg,0,eeeeee,0,eeeeee,.5,ffffff,1', // gradient
    chs: w + 'x' + h
  };

  var url = 'http://chart.apis.google.com/chart?' + join(params);

  return url;
}
```
- example usage
```shell
...
		jslitmus.on('complete', function(test) {
		// Output test results
			currentSet.innerHTML += test + '<br/>';
		});
		// 'all_complete' fires when all tests have finished.
		jslitmus.on('all_complete', function() {
			// Get the results image URL
			var url = jslitmus.getGoogleChart();
			if (currentSet.id === 'small') {
				currentSet.innerHTML += resultTmpl({size: snippet.length, url: url});
				setTimeout(function() {
					jslitmus.clearAll();
					currentSet = document.getElementById('large');
					for(var i=0; i<8; i++) { snippet += snippet; }
					testsetup(snippet);
...
```

#### <a name="apidoc.element.dot.jslitmus.on"></a>[function <span class="apidocSignatureSpan">dot.jslitmus.</span>on (e, f)](#apidoc.element.dot.jslitmus.on)
- description and source-code
```javascript
on = function (e, f) {
  if (!listeners[e]) listeners[e] = [];
  listeners[e].push(f);
}
```
- example usage
```shell
...
		doU = require('./templating/doU.js');
		doT = require('./templating/doT.js');
		var passOne = 0;
		console.log("*** Compilation speed test");
		console.log("*** Small template length: " + snippet.length);
		testsetup(snippet);
		// Log the test results
		jslitmus.on('complete', function(test) {
			//console.log(util.inspect(process.memoryUsage()));
			console.log(test.toString());
		});
		// 'all_complete' fires when all tests have finished.
		jslitmus.on('all_complete', function() {
			switch (passOne) {
			case 0:
...
```

#### <a name="apidoc.element.dot.jslitmus.removeAllListeners"></a>[function <span class="apidocSignatureSpan">dot.jslitmus.</span>removeAllListeners (e)](#apidoc.element.dot.jslitmus.removeAllListeners)
- description and source-code
```javascript
removeAllListeners = function (e) {
  listeners[e] = [];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dot.jslitmus.removeListener"></a>[function <span class="apidocSignatureSpan">dot.jslitmus.</span>removeListener (e, f)](#apidoc.element.dot.jslitmus.removeListener)
- description and source-code
```javascript
removeListener = function (e, f) {
  listeners[e] = filter(listeners[e], function(l) {
    return l != f;
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.dot.jslitmus.runAll"></a>[function <span class="apidocSignatureSpan">dot.jslitmus.</span>runAll (e)](#apidoc.element.dot.jslitmus.runAll)
- description and source-code
```javascript
function runAll(e) {
  forEach(tests, _queueTest);
}
```
- example usage
```shell
...
				break;
			default:
				return;
			}

			jslitmus.clearAll();
			testsetup(snippet);
			jslitmus.runAll();
		});
		// Run it!
		jslitmus.runAll();
	}

	function runTestsInBrowser() {
		jslitmus = window.jslitmus;doU = window.doU;doT = window.doT;
...
```

#### <a name="apidoc.element.dot.jslitmus.test"></a>[function <span class="apidocSignatureSpan">dot.jslitmus.</span>test (name, f)](#apidoc.element.dot.jslitmus.test)
- description and source-code
```javascript
function test(name, f) {
  // Create the Test object
  var test = new Test(name, f);
  tests.push(test);

  // Run the next test if this one finished
  test.on('*', function() {
    // Forward test events to jslitmus listeners
    var args = Array.prototype.slice.call(arguments);
    args.unshift(test._emitting);
    jslitmus.emit.apply(jslitmus, args);

    // Auto-run the next test
    if (test._emitting == 'complete') {
      currentTest = null;
      _nextTest();
    }
  });

  jslitmus.emit('added', test);

  return test;
}
```
- example usage
```shell
...

	var defFolder = this.__path,
		sources = fs.readdirSync(defFolder),
		k, l, name;

	for( k = 0, l = sources.length; k < l; k++) {
		name = sources[k];
		if (/\.def(\.dot|\.jst)?$/.test(name)) {
			if (doT.log) console.log("Loaded def " + name);
			this.__includes[name.substring(0, name.indexOf('.'))] = readdata(defFolder + name);
		}
	}

	for( k = 0, l = sources.length; k < l; k++) {
		name = sources[k];
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
