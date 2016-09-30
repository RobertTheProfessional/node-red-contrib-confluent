#node-red-contrib-confluent

Node-RED (http://nodered.org) nodes for publish/subscribe messaging with Apache Kafka using HTTP(S) calls to the Confluent REST Proxy (https://github.com/confluentinc/kafka-rest).

Works with Apache Kafka 0.9 and 0.10 including Confluent Open Source and Confluent Enterprise distributions (versions 2.0 and 3.0).


#Install

Run the following command in the root directory of your Node-RED install

    npm install node-red-contrib-confluent

Start node-red as normal or use the -v flag for more verbose debugging

	node-red -v

Point your browser to http://localhost:1880

You should see orange confluent input and output nodes in the pallet on the left side of the screen.
<ul>
    <li>input <img src="https://github.com/hjespers/node-red-contrib-confluent/blob/master/images/confluent-in.png"></li>
    <li>output <img src="https://github.com/hjespers/node-red-contrib-confluent/blob/master/images/confluent-out.png"></li>
</ul>

Drag either confluent node to the canvas and double click to configure the topic, key, partition, rest-proxy, clientID and groupID.

<img src="https://github.com/hjespers/node-red-contrib-confluent/blob/master/images/confluent-in-config.png">

Click on the pencil icon to the right of the rest-proxy selection box to configure a rest-proxy URL if one does not already exist.

<img src="https://github.com/hjespers/node-red-contrib-rdkafka/blob/master/images/confluent-rest-proxy-config.png">

Publish and subscribe just as you would with the mqtt node with some small differences namely:
<ul>
	<li>topics should not contain "/" or "." characters
	<li>kafka wildcard/regex subscriptions are not yet fully tested
	<li>ensure you have unique Group IDs configured unless you want multiple consumers to be in a Kafka consumer group
</ul>

#Author

Hans Jespersen, https://github.com/hjespers

#Feedback and Support

For more information, feedback, or support see https://github.com/hjespers/node-red-contrib-confluent/issues