# Koa Static Cache [![Build Status](https://travis-ci.org/jonathanong/koa-static-cache.png)](https://travis-ci.org/jonathanong/koa-static-cache)

Static server for koa.
Caches files' metadata in memory.
Optionally store the memory as well - streams by default.
There is no directory or `index.html` support.

## API

### staticCache(dir, options)

```js
var path = require('path')
var staticCache = require('koa-static-cache')

app.use(staticCache(path.join(__dirname, 'public')), {
  maxAge: 365 * 24 * 60 * 60
})
```

`dir` - the directory you wish to serve.
`options.maxAge` - cache control max age for the files, `0` by default.
`options.buffer` - store the files in memory instead of streaming from the filesystem on each request.

## License

The MIT License (MIT)

Copyright (c) 2013 Jonathan Ong me@jongleberry.com

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.