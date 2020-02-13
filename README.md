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

# Motivation
- Low latency 
- Auto Shard & Scale
- Faster time to market
- Take the Logic to your Data 
- Fast Prototyping while allow hardening for production
  - write clean, focused business logic.

# Architecture
- Message Service Protocol => Supervisor Stream with HR Time Scheduler for CRUD ( Timers are a backlog Queue ) 
- Advanced optimized Functions
  - Registering Functions in parallel that are transpiled to optimzed functions by conext
  
# The Message Service Protocol
- In Memory with De-Duplication
- Ordered, Consistent
- restart able ( Data don't gets muted the DCP is the final Storage Formart it reflects later the Document State from it.
- It Does The Sharding into Nodes.

# Sharding Memcached
First, a quick summary of what we wanted to accompish:

Never service a request on the wrong server.
Allow scaling up and down at will.
Servers refuse commands that they should not service, but
Servers still do not know about each other.
We can hand data sets from one server another atomically, but
There are no temporal constraints.
Consistency is guaranteed.
Absolutely no network overhead is introduced in the normal case.




a routing Protocol
- https://git.rootprojects.org/root/proxy-packer.js
