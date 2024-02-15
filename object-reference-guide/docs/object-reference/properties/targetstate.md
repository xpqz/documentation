




<h1 class="heading"><span class="name">TargetState</span></h1>

| Applies To: | [TCPSocket](../a-z/tcpsocket.md) |
| --- | ---  |


**Description**


The TargetState property reflects the intended final state of a [TCPSocket](../a-z/tcpsocket.md) object. Its possible values are as follows:


| Stream | UDP |
| --- | ---  |
| Client | Open |
| Server | Bound |
| Closed | Closed |


Setting TargetState to Closed is the recommended way to close a socket. It
informs APL that you want the socket to be closed, but only when it is safe to
do so. When all the data has been sent, the [TCPSocket](../a-z/tcpsocket.md) will generate a [TCPClose](../a-z/tcpclose.md) event which, unless
a callback function decides otherwise, will cause the [TCPSocket](../a-z/tcpsocket.md) object to disappear.


To control socket closure, you may execute the following steps:

1. Set TargetState to Closed
2. **Either:**

continue processing **or**
wait (using `⎕DQ`) for the [TCPSocket](../a-z/tcpsocket.md)   to disappear **or**
wait (using `⎕DQ`) for the [TCPClose](../a-z/tcpclose.md)   event


3. continue processing **or**
4. wait (using `⎕DQ`) for the [TCPSocket](../a-z/tcpsocket.md)   to disappear **or**
5. wait (using `⎕DQ`) for the [TCPClose](../a-z/tcpclose.md)   event


