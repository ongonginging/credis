Credis (http://code.google.com/p/credis) is a client library in
plain C written by Jonas Romfelt (jonas at romfelt dot se) for
communicating with Redis (http://code.google.com/p/redis) servers.
Redis is a high performance key-value database, refer to Redis
project page for more information.

Credis aims to be fast and minimalistic with respect to memory
usage. It runs on Linux and should run on most posix like systems.
Porting it to Windows or other platforms should be
straightforward.

To build credis-test and credis shared and static libraries simply
unpack and run:

  make

To run through a number of credis tests run (presupposed that a
Redis server is listening on the default port on localhost):

  ./credis-test

To perform a simplistic performance benchmark test and measure
number of set-commands per second, run:

  ./credis-test 10000

Where 10000 is the number of set-commands to execute.

Running the benchmark and a redis srver instance locally on
my machine (old dual-core AMD64 and 2 GB RAM running Debian)
roughly results in 33000 commands/second. Slightly (10-15%)
faster than the benchmark provided with the redis server.
