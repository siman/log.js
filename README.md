# Log.js

Handy logging wrapper around `window.console` with log levels in JavaScript.

## Why not `console.log()`?

Log.js has a number of extra features comparing to `console.log()`:

* Adds date and time when log was written.
* Adds log level.
* Adds name of a logger. If you have many different loggers in application this feature will be very helpful.
* Message could be passed as a function and it will be called only if appropriate log level is enabled.

## Usage

Include Log.js script in your HTML page:

```html
<script src="/path/to/log-0.0.1.js"></script>
```

And then use it:

```javascript
var myLog = LogJS.get({name: "MyLog", level: "trace", enabled: true});
myLog.info("Hello, Log");
myLog.trace(function() {
    return "Current log level is: " + myLog.getLevel();
});
```

Example of console output:
```
01:48:36.569 INFO  [MyLog] Hello, Log
01:48:36.570 WARN  [MyLog] Hello, Log
01:48:36.570 ERROR [MyLog] Hello, Log
```

## Log levels

Log levels (case insensitive):

1. `TRACE` (the least serious)
2. `DEBUG` (default)
3. `INFO`
4. `WARN`
5. `ERROR`
6. `FATAL` (the most serious)

## Date & Time formatting

Formatting of date and time is done via moment.js
http://momentjs.com/docs/#/displaying/format/

## Required libs

* Moment.js
* JSON

## Inspiration

This library is inspired by `slf4j` and similar logging frameworks from Java world.
