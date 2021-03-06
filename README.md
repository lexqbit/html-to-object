# html-to-object
A lightweight HTML parser for JavaScript that converts your native HTML code into an Array of JavaScript Objects.

## Install
`$ npm install --save html-to-object`

## Usage
```javascript
const h2o = require('html-to-object');

const results = h2o('path/to/file.html', [options]);
```

## Options

#### build (default: false)
Returns the parsed elements as prebuilt DOM nodes to easily append them to the page.
```javascript
const fs = require('fs');
const h2o = require('html-to-object');

const results = h2o('path/to/file.html', { build: true });
```

#### targetIsFile (default: true)
In case of preloaded .html file content.
```javascript
const fs = require('fs');
const h2o = require('html-to-object');

const html = fs.readFileSync('path/to/file.html', 'utf8');
const results = h2o(html, { targetIsFile: false });
```

#### attributesAsObject (default: false)
Will define the attributes property of each element as an Object instead of an Array.
```javascript
const h2o = require('html-to-object');

const results = h2o('path/to/file.html', { attributesAsObject: true });
```


## License
[MIT](LICENSE) © [Max Sandelin](https://github.com/themaxsandelin)
