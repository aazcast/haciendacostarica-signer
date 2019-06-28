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

## EXAMPLE OF USE ASYNC/AWAIT
```js
//Definir la dependencia.
const Signer = require('haciendacostarica-signer');

const nameController = async (req, res) => {
  try {
    //Enviar a .sign el XML en string, la llave criptografica (.p12) en BASE64, y el pass en string.
    //Se retornara el XML ya firmado en BASE64.
    const xml = await Signer.sign(xmlString, llavecriptografica, PassLlaveCriptografica);

    //Tambien está el function verifySignature el cuál verifica que la llave criptografica y el pass de la misma sean correctas, además nos retornara cuando expira la misma.
    //Si es correcto retorna true, caso contrario el error.
    //Ej de uso: antes de guardar los datos del contribuyente y usar el Sign se puede verificar con antelación la llave. Si es true se guarda.
    const verify = await Signer.verifySignature(llavecriptografica, PassLlaveCriptografica);
    //la function verify nos retorna lo siguiente si es correcta y no ha expirado:
    { isValid: true, expiresOn: 2021-06-20T01:29:49.000Z }

  } catch (err) {
    res.send(err);
  }
}

```


## Changelog
[CHANGELOG.md](CHANGELOG.md)

## Donations
https://paypal.me/aazcast

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