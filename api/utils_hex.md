---
layout: api
title: Hex
icon: fa-ellipsis-h
---

Hex
===

Hex object is used to encode/decode text/binary in hexadecimal format.

- Module: **api/utils/hex**
- Definition: [/core_api/issues/19](https://github.com/dirigiblelabs/core_api/issues/19)
- Source: [/api/utils/base64.js](https://github.com/dirigiblelabs/core_api/blob/master/core_api/ScriptingServices/api/utils/hex.js)
- Status: **beta**

Basic Usage
---

```javascript
/* globals $ */
/* eslint-env node, dirigible */

var hex = require('utils/hex');
var response = require('net/http/response');

response.println(hex.encode('Hex Encoded'));
response.println(hex.decode('48657820456e636f646564'));

response.flush();
response.close();
```




Definition
---

### Functions

---

Function     | Description | Returns
------------ | ----------- | --------
**decode(input)**   | Decode an input string from HEX | *string*
**encode(input)**   | Encode an input string to HEX | *string*




Compatibility
---

Rhino | Nashorn | V8
----- | ------- | --------
 ✅  | ✅  | ❌

