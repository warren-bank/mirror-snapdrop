# Snapdrop 

[Snapdrop](https://github.com/SnapDrop/snapdrop): local file sharing in your browser. Inspired by Apple's Airdrop.

##  Classic Snapdrop is built with the following awesome technologies
* Vanilla HTML5 / ES6 / CSS3 frontend
* [WebRTC](http://webrtc.org/) / [WebSockets](http://www.websocket.org/)
* [NodeJS](https://nodejs.org/en/) backend
* [Progressive Web App](https://wikipedia.org/wiki/Progressive_Web_App)

## Self-hosting on LAN

* websocket server
  1. install dependencies:
     ```bash
       cd ./server
       npm install
     ```
  2. start server on port `3000`:
     ```bash
       node ./server/index.js
     ```

* http server
  1. install your favorite web server (for static files)
     - ex: [serve](https://github.com/warren-bank/node-serve)
  2. start server on any available port to serve the [client](./client) directory
     - ex: port `8080`
       ```bash
         serve --cors --listen 8080 ./client
       ```

* http client
  1. open the URL for http server in any modern web browser
     - ex: [http://192.168.0.2:8080/index.html?room=my-private-namespace](http://192.168.0.2:8080/index.html?room=my-private-namespace)
     - where:
       * the value of the `room` querystring parameter is used to group clients
       * any value is allowed
       * when multiple clients connect to the same `room`, then they:
         - are visible to one-another
         - can send files or messages to each other

## License

[GPL-3.0](./LICENSE.txt)
