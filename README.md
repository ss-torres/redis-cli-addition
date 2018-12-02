# redis-cli-addition

Add a move slot function to ease move slot operation

While the main source code is from antirez/redis, I just add a few of functions to move one slot from one node to another node to ease the move slot operation, which needs the specified slot number. I add this function becase the frequency to invoke different keys may be changed a lot, and a few keys occupy the most of invocation. 

To see how to use the function, you can use the redis-cli --cluster help ip:port, and the second last is the function.

The Usage:

The implementation is about redis-5.0.2, and I don't check in other versions. You just replace redis-5.0.2/src/redis-cli.c with this file. Then you could make as usual. 

The output is like:
```
Cluster Manager Commands:
...
  move-slot      from-host:from-port to-host:to-port slotNo
  help
```
