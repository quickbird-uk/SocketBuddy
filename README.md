# SocketBuddy
Cross-protocol real-time API Explorer App

While developing in-house real-time applicaitions is perfectly tractable, when it comes to integrating to third-party APIs
ALL HELL BREAKS LOOSE. It's a fuckign wild west out there, there is no standard documentation tool like swagger, 
and there are almost no established conventions on how you should structure the API like there are in REST. 
Developing real-time software is needlessly difficult and there is no reason for this. 
It is not inherently more complicated, we just lack proper tools. 


Socketbuddy is meant to solve part of the problem - it's a "postman for realtime" and it is meant to allow developers 
to test and explore realitime APIs with the same ease as they do with REST APIs. We will never have proper real-time web untill using these APIs becomes easy. 

### Priorities
* Testability — The app shall enable you to test your API servers and make sure they are doing what you think they are doing
* Exploration — the app shall enable you to explore someone else's APIs and see what they are doing
* Flexebility — the applicaiton shall support multiple protocols, form Websocket to Kafka. 
* Extensible — if you are developer of a messaging system, it should be easy to add your implementation
* Performant — some APIs involve very large volumes of data, and the app has to keep up
* Style — we want a convenient and pretty UI
* We will not, for the time being, deal with unframed streams of data, only with message-based systems. That means we won't support stream websocket for now. 

## Protocols
* Websocket
* Kafka
* MQTT
* WebRTC
* Emitter.io
* RabbitMQ

## Serialisers
* JSON
* Protobuff

## Libraries used
* Dbreeze
* LightInject
* Template 10

## FAQ
### How is development suppose to happen? 
The priority is to have a cross-protocol message-testing applicaiton. We will start by implementing web-scket and Kafka, as 
those are the most common systems. We would like to make it easy to contribute and extend the project with new protocols, while sharing common UI features. 

### Universal Windows? I have a Mac! Microsoft is evil!  
Because we like making windows 10 apps, and they have very good UI performance. 
If there will be demand from non-windows platforms, we will transition it to Xamarin.

### How is development funded 
For the time being, it's a side project. If this becomes really popular, we might add paid 'Enterprise' 
eatures such as team syncing and management, testing, performance benchmarks, running
tests from a cloud server on web-hook request recieved, etc. 
