# Mio Guide App
A simple audio guide. Questions? Contact thomas.amberg@fhnw.ch

## Get the PWA
To get the app, type _mio.guide_ in your browser, or scan the QR code below:

![mio_guide](https://github.com/user-attachments/assets/e25fd27a-31b5-42ca-982b-358791ce84c0)

It points to https://www.mio.guide/ (our generic [PWA](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps)).

## Visit a place
To visit a place, using the app, scan the QR code below:

![mio guide 3rdparty](https://github.com/user-attachments/assets/9171567f-9f6d-4c54-b645-5924bf2e6312)

It points to https://www.mio.guide/reader?url=https://raw.githubusercontent.com/tamberg/guide/main/README.md (3rd party [content](https://raw.githubusercontent.com/tamberg/guide/main/README.md)).

## Add a guide
To add a guide, on your website _example.com_ (or in a [Github](https://github.com/) repo), publish a file _museum.md_ with the following structure:

```md
# Museum
## Room 1
### Work A
Description of work A
### Work B
Description of work B
## Room 2
...
```

Then adapt the URL https://www.mio.guide/reader?url=https://example.com/museum.md and [create a QR code](https://ddg.co/?q=qr+https://www.mio.guide/reader?url=https://example.com/museum.md).

## Build the PWA
To build the PWA from source code, using [Node.js](https://nodejs.org) and [npm](https://npmjs.com), type:
```console
$ npm install
$ npm start
```

## Deploy the PWA
To host the PWA on your domain, deploy to a publicly accessible, static Web server:
```console
$ npm run build
$ cp dist/mio-guide/index.html dist/mio-guide/404.html
$ cp -r dist/mio-guide/* ../www
```
