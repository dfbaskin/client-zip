## 1.1.1
* patch: fixed DOS date/time encoding
* patch: fixed Invalid Date that was attributed to Responses with no Last-Modified header

## 1.1.0
* minor: the WebAssembly Memory is now created inside the wasm module, resulting in a module that is easier to import and a small reduction in bundle size
* typo: removed a little bit of duplicate code in normalizeInput's Response name handling

## 0.3.0
* minor: `input.lastModification` is now optional in all cases
* minor: when extracting the file name from a Request, consider first the "filename" option from the "Content-Disposition" header

## 0.2.4 More Fixed
* patch (**critical**): fixed infinite loop in a function that was trying to chunk large files for crc32

## 0.2.3 Fixed!
* patch (**critical**): computed file size was *NaN* when reading from a stream
* patch: a little mangling and refactoring again

## 0.2.2
* patch: update README with recent changes to property names

## 0.2.1
* patch: a little refactoring and tweaking of Terser options
* actually breaking but I didn't notice: renamed input property `modDate` to `lastModification`

## 0.2 more speed!
* minor: now using WebAssembly for CRC32, yielding a ~10x speed improvement over the JavaScript version
* minor: polyfill *Blob*.stream() instead of using a FileReader to process Blobs
* patch: fix typo in README

## 0.1 First commit
