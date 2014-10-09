node-optval
===========

Tiny module for setting a default value when a parameter is undefind or null.

Shorthand for

```
(typeof(param) === 'undefined' || param === null) ? defaultVal : param
```

The tests say it all...

```
assert.equal('foo', optval('foo'));
assert.equal('foo', optval('foo', 'bar'));

assert.equal('bar', optval(undefined, 'bar'));
assert.equal('bar', optval(null, 'bar'));

assert.equal(undefined, optval(undefined, undefined));
assert.equal(undefined, optval(null, undefined));

assert.equal(null, optval(undefined, null));
assert.equal(null, optval(null, null));
```