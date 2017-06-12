# isnumber

A native module for effectively validating if a value is type Number built on top of a famous library isnumber.

## Usage

```js
var isNumber = require('isnumber-js');

isNumber(5e3)      //=> 'true'
isNumber(0xff)     //=> 'true'
isNumber(-1.1)     //=> 'true'
isNumber(0)        //=> 'true'
isNumber(1)        //=> 'true'
isNumber(1.1)      //=> 'true'
isNumber(10)       //=> 'true'
isNumber(10.10)    //=> 'true'
isNumber(100)      //=> 'true'
isNumber('-1.1')   //=> 'true'
isNumber('0')      //=> 'true'
isNumber('012')    //=> 'true'
isNumber('0xff')   //=> 'true'
isNumber('1')      //=> 'true'
isNumber('1.1')    //=> 'true'
isNumber('10')     //=> 'true'
isNumber('10.10')  //=> 'true'
isNumber('100')    //=> 'true'
isNumber('5e3')    //=> 'true'
isNumber(parseInt('012'))   //=> 'true'
isNumber(parseFloat('012')) //=> 'true'
```

### False

```js
isNumber('foo')             //=> 'false'
isNumber([1])               //=> 'false'
isNumber([])                //=> 'false'
isNumber(function () {})    //=> 'false'
isNumber(Infinity)          //=> 'false'
isNumber(NaN)               //=> 'false'
isNumber(new Array('abc'))  //=> 'false'
isNumber(new Array(2))      //=> 'false'
isNumber(new Buffer('abc')) //=> 'false'
isNumber(null)              //=> 'false'
isNumber(undefined)         //=> 'false'
isNumber({abc: 'abc'})      //=> 'false'
```

## Installation

With [npm](https://npmjs.org) do

```bash
$ npm install isnumber-js
```

Then bundle for the browser with
[browserify](https://github.com/substack/node-browserify).

## License

(MIT)

Copyright (c) 2017 Nejc Trnjanin &lt;zlatinejc@gmail.com&gt;

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies
of the Software, and to permit persons to whom the Software is furnished to do
so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.