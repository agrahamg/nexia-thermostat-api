Nexia-thermostat-api
=========
An api to control nexia thermostats


Usage
=====

* connect using a mobile id from nexia site
* use api.getHouse() to load basic info
* use commands
 

API
===
to be added soon


Activation
==========

To get the mobile ID and the api key you have to do the following:

1) Login to mynexia.com
2) Go the to Mobile tab
3) Create a new mobile device
4) Click the Get Activation code button for the new mobile device
5) Make a call to `NexiaApi.connect(activation_code)` and log the output

```js
const nexiaApi = require('nexia-api');

const activation_code = 12345;  // get this from the web ui by following directions above

nexiaApi.connect(activation_code).then((api) => {
  console.log(api);
}).catch((e) => {
  console.error(e);
});
```