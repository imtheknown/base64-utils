
# Base64 Utils

Utility module to perform various operations on a base64 string

## Installation

```
 $ npm install base64-utils 
 ```

 ## Usage

 ```js
 const base64Utils = require("base64-utils");
//or
import * as base64Utils from "base64-utils"
```

## API

### isValidBase64
Checks if the base64 string is valid.

```js
base64Utils.isValidBase64("SGVsbG8gV29ybGQ"); //returns false

base64Utils.isValidBase64("SGVsbG8gV29ybGQ="); //returns true
```
### getMimeType
Tries to read mimetype of a base64 string, returns mimetype if found, otherwise returns a empty string.

```js
base64Utils.getMimeType("data:image/png;base64,iUgAAAAUAAAAF=="); //returns "image/png"

base64Utils.getMimeType("SGVsbG8gV29ybGQ="); //returns ""
```
### Conversion Methods
To Convert Base64 String to different data formats

```js
//Convert Base64 to Buffer
base64Utils.base64ToBuffer("SGVsbG8gV29ybGQ="); 
//Convert Base64 to UTF8
base64Utils.base64ToUtf8("SGVsbG8gV29ybGQ=");
//Convert Base64 to Hex
base64Utils.base64ToHex("SGVsbG8gV29ybGQ="); 
//Convert Base64 to Binary
base64Utils.base64ToBinary("SGVsbG8gV29ybGQ=");   
```
