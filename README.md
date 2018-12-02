# redis-cli-addition

Add a move slot function to ease move slot operation

While the main source code is from antirez/redis, I just add a few of functions to move one slot from one node to another node to ease the move slot operation, which needs the specified slot number. I add this function becase the frequency to invoke different keys may be changed a lot, and a few keys occupy the most of invocation. 

To see how to use the function, you can use the redis-cli --cluster help ip:port, and the second last is the function. 

The output is like:
```
Cluster Manager Commands:
...
  move-slot      from-host:from-port to-host:to-port slotNo
  help
```
