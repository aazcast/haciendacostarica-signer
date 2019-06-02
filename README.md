# haciendacostarica-signer
> A Node.js implementation to sign with XADES-EPES the Electronic Bill Hacienda Costa Rica using the .p12 file and password.

## Credits
https://github.com/PeculiarVentures/xadesjs/issues/54
and
Andrés Castillo @aazcast from gravity.cr

## Install
```sh
$ npm i haciendacostarica-signer --save
```

## USE
```js
const Signer = require('haciendacostarica-signer');
const xml = await Signer.sign(xmlString, llavecriptografica, PassLlaveCriptografica);

const verify = await Signer.verifySignature(llavecriptografica, PassLlaveCriptografica);
```

## Changelog
[CHANGELOG.md](CHANGELOG.md)

## License
The MIT License (MIT)

Copyright (c) 2019 Andres Castillo (andres@gravity.cr)

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.