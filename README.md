# LetraTag label printer

A single-page web app for printing labels on a **DYMO LetraTag LT-200B** over Bluetooth, straight from the browser. No app, no install, no server.

**Open it:** https://bartoszbielawski.github.io/letratag/

Works in **Chrome or Edge** on macOS, Windows, Linux and Android. Safari and Firefox (and therefore iPhones) don't support Web Bluetooth.

## Features

- Any font your computer has, plus a set of web fonts
- Symbols and emoji anywhere in the text (printed as silhouettes), with a picker and recent row
- Image files, dithered or black & white
- Code 128 and EAN-13 barcodes
- Date placeholders: `{date}`, `{date+7}`, `{date+2w}`, `{date+1m}`, `{time}`
- Fixed label length with left/center/right alignment
- Vertical labels with stacked upright letters
- Mirror mode for stickers on the inside of glass
- White on black, frame, copies
- Real-size preview with a ruler (calibrate once with a bank card)
- Remembers your last printed labels

## Using it

1. Open the page in Chrome or Edge and switch the printer on.
2. Click **Connect printer** and pick the LetraTag from the list.
3. Type your label and click **Print**.

To run it locally instead, Chrome needs the page served from `localhost`:

```bash
python3 -m http.server 8000 --bind 127.0.0.1
```

Then open http://localhost:8000/.

## Credits

The printer protocol comes from [ysfchn/dymo-bluetooth](https://github.com/ysfchn/dymo-bluetooth) by Yusuf Cihan, MIT License. Its license notice is included at the top of `index.html`.

Not affiliated with, endorsed or supported by DYMO. DYMO and LetraTag are trademarks of their respective owners.
