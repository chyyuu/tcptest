This is a Google Summer of Code project.


## WHAT ##
> A multi-platform TCP/IP v4 Stack Testing Tool,

> As a testing tool, it can perform regression, protocol conformance, and fuzz tests. The tool may also be employed as an aid to protocol developers and both testing and debugging of firewalls/routers.


## USING ##
> It's built on top of PCS(Packet Construction Set)

> "PCS is a set of Python modules and objects that make building network protocol code easier for the protocol developer. The core of the system is the pcs module itself which provides the necessary functionality to create classes that implement packets." http://pcs.sourceforge.net/

> PCS enables testing at OSI layers 3, 4, and 5.


## HOW ##
> Tcptest mainly is a python module and one script for each test covered (more then one per script often)
> The module count with methods acting as fasteners, doing things like (a)three way handshake, (b)active/passive close and (c)several createXX and assertXX, where XX=(ip, tcp, rst, urg, fin, syn, psh, so on...)
> As the tests are being created, the number of 'fasteners' are growing, turning each moment easier to create new tests.


## PHILOSOPHY ##
> Use of small tests. So we can cover a wide range of traffics, events and transitions predetermined separately.

> The development would be like a protocol, but without covering all possible events and transitions, only traffic previously determined.

> Instead of targeting a TCP Finite State Machine (FSM) like the implementation of TCP/IP protocols, the development will be based towards flow of packets, where traffic is composed of packets that are sent and received in a previously registered way.


## THE FOLLOWING TESTS WILL BE INITIALLY COVERED ##
  1. Three-way handshake
  1. Reset from closed state
  1. Reset from non syncronized state
  1. Reset from syncronized state
  1. Sliding Window Protocol
  1. Urgent Pointer
  1. TCP Options establishment
  1. Selective Acknowledgments
  1. TCP Timestamps
  1. Time-wait configuration
  1. Connection close
  1. Simultaneous close
  1. Receive Window Size Advertisement
  1. Transmit Window Size Advertisement
  1. Support Partner’s Shrinking Window
  1. Silly Window Syndrome Avoidance
  1. Zero Window Handling
  1. Receive ACKs, RSTs, and URGs while Window is Zero
  1. Zero window Probing


## MENTOR ##
  * George Neville-Neil


## STUDENT ##
  * Victor Hugo Bilouro