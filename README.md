# cheerio

This is a version of [sha256](https://github.com/emn178/js-sha256) for Parse.com

## Usage

1. Put 'sha256.js' file into your 'cloud/modules/' folder.
2. Require module in Cloud Code:

```JavaScript
var sha256 = require('cloud/modules/sha256');
```

or

```JavaScript
var sha256 = require('cloud/modules/sha256').sha256;
var sha224 = require('cloud/modules/sha256').sha224;
```

## Example

Code

```JavaScript
sha256('');
sha256('The quick brown fox jumps over the lazy dog');
sha256('The quick brown fox jumps over the lazy dog.');
sha224('');
sha224('The quick brown fox jumps over the lazy dog');
sha224('The quick brown fox jumps over the lazy dog.');
```

Output

    e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855
    d7a8fbb307d7809469ca9abcb0082e4f8d5651e46d3cdb762d02d0bf37c9e592
    ef537f25c895bfa782526529a9b63d97aa631564d5d789c2b765448c8635fb6c
    d14a028c2a3a2bc9476102bb288234c415a2b01f828ea62ac5b3e42f
    730e109bd7a8a32b1cb9d9a09aa2325d2430587ddbc0c38bad911525
    619cba8e8e05826e9b8c519c0a5c68f4fb653e8a3d8aa04bb2c8cd4c

It also supports UTF-8 encoding:

Code

```JavaScript
sha256('中文');
sha224('中文');
```

Output

    72726d8818f693066ceb69afa364218b692e62ea92b385782363780f47529c21
    dfbab71afdf54388af4d55f8bd3de8c9b15e0eb916bf9125f4a959d4

It also supports byte Array input:

Code

```JavaScript
sha256([]);
```

Output

    e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855
