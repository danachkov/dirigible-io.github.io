---
layout: api
title: Digest
icon: fa-ellipsis-h
---

Digest
===

Digest object is used to encript binary/text with algorithms like md5, sha256 and sha512.

- Module: **utils/digest**
- Definition: [/core_api/issues/20](https://github.com/dirigiblelabs/core_api/issues/20)
- Source: [/utils/digest.js](https://github.com/dirigiblelabs/core_api/blob/master/core_api/ScriptingServices/utils/digest.js)
- Status: **beta**

Basic Usage
---

```javascript
/* globals $ */
/* eslint-env node, dirigible */

var digest = require('utils/digest');
var response = require('net/http/response');

response.println("" + digest.sha256('admin:admin'));
response.println("" + digest.sha512('YWRtaW46YWRtaW4='));

response.flush();
response.close();
```





Definition
---

### Functions

---

Function     | Description | Returns
------------ | ----------- | --------
**md5(input)**   | Calculates the MD5 digest and returns the value as a 16 element byte array | *array of byte*
**md5Hex(input)**   | Calculates the MD5 digest and returns the value as a 32 character hex string | *string*
**sha(input)**   | Returns an SHA-1 digest | *array of byte*
**sha1(input)**   | Returns an SHA-1 digest | *array of byte*
**sha256(input)**   | Returns an SHA-256 digest | *array of byte*
**sha384(input)**   | Returns an SHA-384 digest | *array of byte*
**sha512(input)**   | Returns an SHA-512 digest | *array of byte*
**shaHex(input)**   | Calculates the SHA-1 digest and returns the value as a hex string | *string*




Compatibility
---

Rhino | Nashorn | V8
----- | ------- | --------
 ✅  | ✅  | ❌

