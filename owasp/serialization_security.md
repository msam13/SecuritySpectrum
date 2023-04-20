# Insecure Serialization

Owasp 2017 has insecure serialization at 8th position, now in 2021 it reframed as Software and Data integrity failure.

Distributed systems exchanges objects, often object are serialized at one end and deserialized at another end. Insuffient validation of byte stream leads to security risks, like remote code execution, compromise of CIA.

This attack technique is applicable for
-  Any client-server application that exchanges objects
- Thick clients that exchanges data with each other indirectly via a server

Attacker can send evil object to server
- Using debugger to run the application at client side and injecting evil object
- Write an own app, that implements messaging protocols
- intercept the traffic, modify the traffic and inject evil object (MiTM)

In serialization context, input refers to serialized data

Let's consider BinaryFormatter

Binary formatter, converts Binary format to/from Object format. There are 2 functions Serialize and Deserialize 

serialized data will contain 
- Name of the class
serialized data will not contain 
- code for constructor or destructors
- code for getter or setters
- Hash of serialized data

Constructors Types 
- static constructors
- default constructors 

## Deserialization
 
Object stream can be deserialized and type casted in different ways (assume fmt as Binary formatter object and ms as stream of data)
- fmt.Deserialize(ms) as OBJECT
- (OBJECT) fmt.Deserialize(ms)
- fmt.Deserialize(ms)

constructor never get called at the deserialization end

whenever you deserialize destructor get called always
whenever you deserialized destructor is called always

when we are expecting a object of class typeA and deserialize method recieves stream of object of class TypeB, then
- static constructor is called (if existed)
- destructor is always called