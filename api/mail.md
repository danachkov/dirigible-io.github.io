---
layout: api
title: Mail
icon: fa-ellipsis-h
---

Mail
===

Mail object is used to send e-mails through the mail service.

- Module: **service/mail**
- Definition: [/core_api/issues/12](https://github.com/dirigiblelabs/core_api/issues/12)
- Source: [/service/mail.js](https://github.com/dirigiblelabs/core_api/blob/master/core_api/ScriptingServices/service/mail.js)
- Status: **beta**

Basic Usage
---

```javascript
/* globals $ */
/* eslint-env node, dirigible */

var mail = require('service/mail');
var response = require('net/http/response');

var from = "dirigiblelabs@eclipse.org";
var to = "example@gmail.com";
var subject = "Subject";
var content = "Content";

mail.send(from, to, subject, content);

response.println("Mail sent");
response.flush();
response.close();
```


Definition
---

### Functions

---

Function     | Description | Returns
------------ | ----------- | --------
**send(from, to, subject, content)**   | Sends an e-mail with the given subject and content to the given recipient(s) from a given sender | -



Compatibility
---

Rhino | Nashorn | V8
----- | ------- | --------
 ✅  | ✅  | ❌
