# objectid-purejs
Simple implementation MongoDB ObjectID in pure javascript for Node.js

This module as been extracted from BSON (https://github.com/mongodb/js-bson) for a single file to work direct (and only) with an ObjectID.

A simple example of how to use ObjectID in `node.js`:

```js
var ObjectId = require('objectid-purejs');

//Create a new ObjectId
var myId = new ObjectId();

console.log(myID);

```

## Installation

`npm install objectid-purejs`

### ObjectId

**`ObjectId.isValid(id)`** - Returns true if `id` is a valid number or hexadecimal string representing an ObjectId.
**`ObjectId.createFromHexString(hexString)`** - Returns the ObjectId the `hexString` represents.
**`ObjectId.createFromTime(time)`** - Returns an ObjectId containing the passed time.
* `time` - A Unix timestamp (number of seconds since the epoch).

**`var myId = new ObjectId(id)`** - Creates a new `ObjectId`.
* `id` - Must either be a 24-character hex string or a 12 byte binary string.

**`myId.toJSON()`**
**`myId.toString()`**
**`myId.toHexString()`** - Returns a hexadecimal string representation of the ObjectId.

**`myId.equals(otherObjectId)`** - Returns true if the ObjectIds are the same, false otherwise.

**`myId.getTimestamp()`** - Returns a `Date` object containing the time the objectId was created for.
