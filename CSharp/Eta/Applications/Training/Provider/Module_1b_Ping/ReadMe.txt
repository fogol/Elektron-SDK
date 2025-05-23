Transport API Interactive Provider Training Application Description

Module 1b: Ping (heartbeat) Management

--------
Summary:
--------

In this module, after establishing a connection, ping messages might
need to be exchanged. The negotiated ping timeout is available via
the Channel. If ping heartbeats are not sent or received within
the expected time frame, the connection can be terminated. LSEG
recommends sending ping messages at intervals one-third the
size of the ping timeout.

Detailed Descriptions:

Once the connection is active, the consumer and provider applications
might need to exchange ping messages. A negotiated ping timeout is available
via Channel corresponding to each connection (this value might differ on
a per-connection basis). A connection can be terminated if ping heartbeats
are not sent or received within the expected time frame. LSEG
recommends sending ping messages at intervals one-third the size of the ping timeout.

Ping or heartbeat messages are used to indicate the continued presence of
an application. These are typically only required when no other information is
being exchanged. Because the provider application is likely sending more frequent
information, providing updates on any streams the consumer has requested,
it may not need to send heartbeats as the other data is sufficient to announce
its continued presence. It is the responsibility of each connection to manage
the sending and receiving of heartbeat messages.

-----------------
Application Name:
-----------------

ProvMod1b

------------------
Setup Environment:
------------------

No additional files are necessary to run this application.

-------------------
Command line usage:
-------------------

dotnet run

Runs with a default set of parameters (-p 14002)

or

dotnet run -- [-p <SrvrPortNo>]

To view all command-line options, run:

dotnet run -- -?

Pressing the Ctrl+C buttons terminates the program.

-----------------
Compiling Source:
-----------------

The included project file is set up to run from the file locations as presented
through the distribution package.

To compile, run the `dotnet build` command with desired parameters
(configuration, architecture, etc.)

For windows platform, using Visual Studio, open the main ETA.NET.sln solution
file and build the ProvMod1b project.

----------------
Example Content:
----------------

Included for this application are:

- Source files.

- This document.

--------------------
Detailed Description
--------------------

Module_1b_Ping.cs - The main file for the Transport API Interactive Provider Training application.
