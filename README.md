# NODE-DOCUMENT-VALIDATOR-JSONSCHEMA [![Build Status](https://secure.travis-ci.org/grimen/node-document-validator-jsonschema.png)](http://travis-ci.org/grimen/node-document-validator-jsonschema)

**Validator** adapter [json-schema](https://github.com/kriszyp/json-schema) for [node-document](https://github.com/grimen/node-document) ODM for Node.js.


## Installation

```shell
  $ npm install node-document-validator-jsonschema
```


## Usage

**Basic:**

```javascript
  var Validator = require('node-document-validator-jsonschema');

  var validator = new Validator();

  var data = {
    foo: "foo",
    bar: 123,
    baz: undefined
  };

  var schema = {
    foo: {
      type: "string",
      minLength: 4
    },
    bar: {
      type: "number"
    },
    baz: {
      required: true
    }
  };

  validator.validate(data, schema, function(err, errors, valid) {
    console.log("Valid: %s  \nErrors:\n", valid, errors);
  });
```

For details; see [node-document](https://github.com/grimen/node-document).


## Test

**Local tests:**

```shell
  $ make test
```


## License

Released under the MIT license.

Copyright (c) [Jonas Grimfelt](http://github.com/grimen)
