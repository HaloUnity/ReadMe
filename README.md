##Mission Statement

HaloUnity strives to create an opensource subset of Halo 3 that offers an authorative distributed server (client-server) model with an emphasis on ranked and unranked matchmaking.

##Technologies

###Game Engine
https://unity3d.com/ Unity3D is a free, modern and productive game engine to develop applications in. Offering C#/.NET at the scripting layer provides for unparalleled productivity.

###Networking
https://github.com/HelloKitty/GladNet2.0 GladNet2 is an in-development networking API that can be implemented around other lower level networking libraries. Specifically HaloUnity will be utilizing GladNet2 with Lidgren underneath. The reasoning for this is not only licensing, platform deployment and bandwidth considerations but most importantly it matches the requirement of the network protocol of Halo 3.

###Networking Protocol
http://gamedevs.org/uploads/tribes-networking-model.pdf HaloUnity will implement the TRIBES Networking Protocol. GladNet2.Lidgren is a perfect networking library to implement this protocol as Lidgren offers reliable/unreliable UDP with the ability to designate ordering or discarding stale packets. These meet the four main transmission criteria for implementing the TRIBES protocol.

Why are we using the TRIBES Protocol? This is because Halo 3 and Halo Reach are based on this protocol and is a proven protocol which is discussed in the GDC talk about Halo: Reach Networking http://www.gdcvault.com/play/1014345/I-Shot-You-First-Networking

###Physics
This is a difficult decision. Physx is all that is currently available in Unity3D however it's well known Halo is built upon the Havok physics engine. It is out of the scope of this project to integrate Havok with Unity3D by writing a C# wrapper. Nobody will stop you from doing so but getting parity with Physx in Unity, which isn't even the full Physx, would be a difficult challenge. Physx 3.x in Unity5 should suffice

###Graphics
Halo 3 graphics pipeline was incredibly complex. It would take a small team of professional programmers awhile to implement the material and lighting system of Halo 3 in Unity. This is likely out of the scope of HaloUnity however if great minds come together, preferably ones with degrees in Mathematics, then it may be possible. Halo 3 uses a Cook Torrance BRDF material system with Spherical Harmonic lightmaps. We can get approximations with Unity5's Enlighten GI but it's not as close as one would like. If you're up for the challenge the material and lighting solution is partially described in this paper http://amd-dev.wpengine.netdna-cdn.com/wordpress/media/2013/01/Chapter01-Chen-Lighting_and_Material_of_Halo3.pdf and other referenced papers.
