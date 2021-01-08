# generate-datamatrix

Data Matrix Codes are a type of 2D codes that are used frequently in industrial spaces,
as they can encode a large amount of information in a small footprint. This code minimally implements
the encoding of a barcode. It's left to the end user to adapt this into using a graphics library for
rendering to a display or image file.

## Example

```
const DataMatrix = require('../main');

const datamatrix = new DataMatrix();

datamatrix.encodeAscii('Hello World!');

// Or, datamatrix.encodeX11 for alphanumeric and a few add'l characters.
// datamatrix.encodeX11('HELLO WORLD');

console.log(datamatrix.renderAscii());

// Or, datamatrix.renderPBM for a Portable BitMap
```

## Resulting Text
```
████████████████████████████████████
██  ██  ██  ██  ██  ██  ██  ██  ████
██  ██    ██    ██    ██  ██████  ██
██    ██████    ██  ██  ████████████
██      ██    ████████████    ██  ██
██    ██████████  ████  ████    ████
██      ██████  ██  ██████  ██    ██
██    ████    ██████    ██  ████████
██      ██    ██  ████  ██  ████  ██
██  ████  ██  ██      ██  ██████████
██  ██    ██        ████  ██  ██  ██
██      ██    ████  ██  ██  ████████
██  ██        ████████  ██  ██    ██
██  ██    ██  ██  ██  ████    ██████
██    ████████                ██  ██
██    ██      ██  ██  ██  ████  ████
██                                ██
████████████████████████████████████
```


## Basic Support

Currently, only ASCII and X12 encoding is supported. The Data Matrix specification includes a number of additional
codewords that improve efficiency for reduced character sets. Output is either ASCII or PBM.

## One dependency

It's just a few hundred lines of clear, readable, code; and relies on reed-solomon-datamatrix.

## Also Free

Licensed under Apache 2.0

