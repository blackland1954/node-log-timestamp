log-timestamp
=============

Prepend timestamps to functions like console.log, console.warn, etc

Example
-------

``` js
console.log('Before log-timestamp');
require('log-timestamp');
console.log('After log-timestamp');
```

yields

```
Before log-timestamp
[2012-08-23T20:08:32.000Z] After log-timestamp
```

You can specify a custom function as well

``` js
require('log-timestamp')(function() { 'date="' + Date.now() + '" message="%s"');
console.log('hello %s', 'world');
```

yields

```
date="2012-08-23T20:08:37.000Z" message="hello world"
```

Install
------

    npm install log-timestamp

Tests
-----

    npm test

License
-------

MIT License
