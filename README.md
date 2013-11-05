# Log.js

JavaScript logging framework with log levels

## Required libs

* Moment.js
* JSON

## Usage

Include Log.js script in your HTML page:

```html
<script src="./log-0.0.1.js"></script>
```

And then use it:

```javascript
var myLog = LogJS.get({name: "MyLog", level: "trace", enabled: true});
myLog.info("Hello, Log");
myLog.trace(function() {
    return "Current log level is: " + myLog.getLevel();
});
```

## Date & Time formatting

Formatting of date and time is done via moment.js
http://momentjs.com/docs/#/displaying/format/

## Inspiration

This library is inspired by 'slf4j' and similar logging frameworks from Java world.
