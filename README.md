# es-NetworkCluster
ECMAScript Implamentation of SocketCluster like concepts for any network layer is the foundation of es-SocketNetwork a dropin replacement for the old CJS based SocketCluster Project


This forms a mesh out of many instances that runs any kind of server via sharing a single state of broker instances aka service discovery and then 

Algo:
- Register instances on a single point
- Retrive instances from a single point
- Share messages with other Instances 
  - Retrive instances also via internal messages
  
yes its a distributedMessageBus this can be used with JSON Data or Grpc or HTTP2 WebRTC

Its also the basic building block of a service mesh or a network mesh

the limits? a broker can handle x connections including the connections to other brokers next scaling option is sharding to unlimited.this is what for example couchbase, and kafka do.
