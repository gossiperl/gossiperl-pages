# language agnostic, Apache Thrift based gossip middleware and message bus

####pronounced [ `gossip,erl ]
  
The purpose of gossiperl is to provide a gossip as a service for applications running on a host.

Gossiperl is written in Erlang. Once a gossiperl daemon is compiled and installed on the host, an application can connect and start exchanging data with other members. This is achieved by applications registering their own overlays. Every overlay can be secured using dedicated symmetric key. Only the member who has access to a given symmetric key, has access to the data exchanged on that overlay. Additionally, every gossip client uses their own secret key to prevent spoofing by other overlay members. Messages between applications can be shared only via gossiperl daemon. The daemon knows the secret keys of every application and will not attempt passing any messages from the application if the key doesn’t match.

Every overlay uses its own separate configuration. Such overlays behave as completely separate systems.

Gossiperl client applications can publish and subscribe to digest types provided by other applications.

Created by Rad Gruchalski, 2014
MIT license

- [Source code](https://github.com/gossiperl/gossiperl)
- [Documentation](https://github.com/gossiperl/gossiperl/wiki)