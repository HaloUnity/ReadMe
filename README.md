##Mission Statement

HaloUnity strives to create an opensource subset of Halo 3 that offers an authorative distributed server (client-server) model with an emphasis on ranked and unranked matchmaking.

##Technologies

Game Engine - https://unity3d.com/ Unity3D is a free, modern and productive game engine to develop applications in. Offering C#/.NET at the scripting layer provides for unparraled productivity.

Networking - https://github.com/HelloKitty/GladNet2.0 GladNet2 is an indevelopment networking API that can be implemented around other lower level networking libraries. Specifically HaloUnity will be utilizing GladNet2 with Lidgren underneath. The reasoning for this is not only licensing, platform deployment and bandwidth considerations but most importantly it matches the requirement of the network protocol of Halo 3.

Networking Protocol - http://gamedevs.org/uploads/tribes-networking-model.pdf HaloUnity will implement the TRIBES Networking Protocol. GladNet2.Lidgren is a perfect networking library to implement this protocol as Lidgren offers reliable/unreliable UDP with the ability to designate ordering or discarding stale packets. These meet the four main transmission critieria for implementing the TRIBES protocol.
