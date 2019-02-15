### MQTT.js
---
https://github.com/mqttjs/MQTT.js

```
npm install mqtt --save

npm install mqtt -g
mqtt sub -t 'hello' -h 'test.mosquitto.org' -v
mqtt pub -t 'hello' -j 'test.mosquitto.org' -, 'from MQTT.js'

npm install -g browserify
cd node_modules/mqtt
npm install .
browserify mqtt.js -s mqtt > browserMqtt.js

npm install -g webpack
cd node_modules/mqtt
npm install .
webpack mqtt.js ./browserMqtt.js --output-library mqtt
```

```js
var mqtt = require('mqtt')
var client = mqtt.connect('mqtt://test.mosquitto.org')

client.on('connect', function () {
  client.subscribe('presence', function (err) {
    if (!err) {
      client.publish('presence', 'Hello mqtt')
    }
  })
})

client.on('message', function (topic, message){
  console.log(message.toString())
  client.end()
})

var mqtt = require('mqtt')
var client = mqtt.connect(wxs://test.mosquitto.org)

import { connect } from 'mqtt';
const client = connect('wxs://test.mosquitto.org');

var mqtt = require('mqtt')
var client = mqtt.connect('alis://test.mosquitto.org')

import { connect } from 'mqtt';
const client = connect('alis://test.mosquitto.org');

var client = mqtt.connect()
client.subscribe("mqtt/demo")

client.on("message", function (topic, payload) {
  alert([topic, payload].join(": "))
  client.end()
})

clinet.publish("mqtt/demo", "hello world!")

var awsIotUrlSigner = require('awsIotUrlSigner')
mqtt.connect('wss://a2ukbzaqo9vbpb.iot.ap-southeast-1.amazonaws.com/mqtt', {
  transformWsUrl: function (url, options, client) {
    return awsIotUrlSigner(url)
  }
})
```

```json
{
  protocolId: 'MQIsdp',
  protocolVersion: 3
}
```


