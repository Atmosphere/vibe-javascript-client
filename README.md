# React
The **React** is a concise, lightweight and feature-rich JavaScript library for real-time web application development. The <strong>React</strong> provides socket for browser-based and Node.js-based applications that need two-way communication with servers, but also aims to utilize a full duplex connection for modern web application development.

The **React** greatly simplifies things essential to real-time web applications like connection sharing, reply, heartbeat and disconnection detection. The <strong>React</strong> is designed by carefully considering known issues and best practices of real-time web to provide a reliable socket based on its simple protocol.

* Website: http://atmosphere.github.io/react-js/

## Test suite

Since this project follows Test Driven Development (TDD) principles well, looking at and running the test suite is a best way to understand the react deeply. Every test has a title specifying a single behavior and is wrriten in QUnit.

* [`client.js`](https://github.com/atmosphere/react-js/blob/master/test/webapp/unit/client.js): Tests react and socket using dummy and mock transport.
* [`server.js`](https://github.com/atmosphere/react-js/blob/master/test/webapp/unit/server.js): Tests transports by interacting with react server. 

### Running

In order to run test suite, you need to have Node.js or write your react server.

Clone this repository or simply download it as a zip and extract it.

```bash
git clone https://github.com/atmosphere/react-js.git
cd react
```

Install dependencies. If you are on Windows, you may have trouble in installing Contextify. See a [installation guide](https://github.com/tmpvar/jsdom#contextify) from jsdom.

```bash
npm install
```

Start server on localhost at port 8080 and 8090. Both servers serve static assets but react server is on 8080.

```bash
node test/server
```

#### As browser client
Open [http://localhost:8080](http://localhost:8080) for same origin or [http://localhost:8090](http://localhost:8090) for cross origin in a browser.

#### As Node.js client
Type `node test/index` in other console.

### Writing server

A server passing the test suite is a very react server. Writing react server is not such hard. One of the goals of this project from day 1 (jquery-stream) is easy to implement in server-side as simple as dealing with Ajax. As various transports and features are added, it gets harder than dealing with Ajax, but still quite easy comparing to other similar projects.

Anyway, the react server used to develop react.js is a good tutorial to write react server and less than 2KB minified and gzipped though it doesn't matter. Check out [server.js](https://github.com/atmosphere/react-js/blob/master/test/server.js).