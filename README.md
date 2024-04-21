# Cloud Computing Concepts - Code Structure Overview

This document explains the general code structure for the cloud computing concepts course assignment, focusing on the provided template.

## Three-Layer Architecture

### The code utilizes a three-layer architecture to separate functionalities:

**Emulated Network (EmulNet):** This layer provides functions to simulate a network environment. It handles sending and receiving messages between peers.
**Application:** This layer drives the overall simulation. It manages tasks like peer startup, crashes, and node loops.
**P2P Layer (MP1Node):** This core layer is where the protocol logic is determined.

## Code Files

### The project consists of the following files

**EmulNet.h:** Contains header information for the Emulated Network layer functions.
**EmulNet.cpp:** Implements the Emulated Network functionalities.
**Application.h:** Contains header information for the Application layer functions.
**Application.cpp:** Implements the Application layer functionalities.
**MP1Node.h:** Contains header information for the P2P layer (MP1Node) class.
**MP1Node.cpp:** Implements the P2P layer functionalities within the MP1Node class.
**Log.h:** Contains header information for logging functions.
**Log.cpp:** Implements the logging functionalities (LOG function).
**Member.h:** Contains header information for member functions.
**Member.cpp:** Implements the member information management functions.
**Params.h:** Contains header information for simulation parameters functions.
**Params.cpp:** Implements the functions to configure and manage the simulation parameters.
**Queue.h:** A wrapper for a custom queue implementation.
**stdincludes.h:** Provides a central location to define project-wide constants, include standard library headers, and potentially configure debugging options.

## P2P Layer (MP1Node) Class

The MP1Node class is central to the implementation. It interacts with the Emulated Network layer and the Application layer.

**nodeLoopOps():** This function handles periodic operations within the membership protocol logic. It's called repeatedly during the simulation.
**recvCallBack(message):** This function is triggered when the node receives a message from another peer. It's responsible for processing the received message based on your protocol.
