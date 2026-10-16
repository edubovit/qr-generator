# QR generator

A simple, single-page QR generator. No build step, backend, or uploads.

## Use

Open `index.html` in your browser, paste text or select a local file, then click **Generate QR**. Download the result as a PNG.

- **Text files:** encodes UTF-8 contents directly.
- **Binary files:** encodes a data URL; requires a compatible reader, not a hosted download link.
- **Limit:** 2,331 UTF-8 bytes per QR code. Binary encoding adds overhead.

Contents stay in your browser. An internet connection is required to load the pinned [qrcode-generator](https://github.com/kazuhikoarase/qrcode-generator) library from jsDelivr.

## Verification

Browser-tested via localhost: text and file round trips with an independent QR decoder, Unicode, payload limits, validation, PNG download, clear/reset, and mobile layout. Direct `file://` opening was not covered by the automated browser tests.
