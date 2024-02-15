




<h1 class="heading"><span class="name">LocalPort</span></h1>
| Applies To: | [TCPSocket](../a-z/tcpsocket.md) |
| --- | ---  |

| Applies To: | [TCPSocket](../a-z/tcpsocket.md) | [TCPSocket](../a-z/tcpsocket.md) |  |  |
| --- | --- | ---  |
| [TCPSocket](../a-z/tcpsocket.md) |  |  |


Description


The LocalPort property is a scalar integer in the range 1-65536 that
identifies the port number associated with a [TCPSocket](../a-z/tcpsocket.md)
 object.



Note that you may use *either* LocalPort *or* [LocalPortName](../a-z/localportname.md)
 to identify the service. The use of [LocalPortName](../a-z/localportname.md)
 is slightly slower but it avoids hard-coding the port number in your program and
is generally more flexible. If you specify both properties, the value of [LocalPortName](../a-z/localportname.md)
 will be ignored.


LocalPort may be specified only by the process that is initiating the
connection (the server) and must be set by the `⎕WC`
statement that creates the [TCPSocket](../a-z/tcpsocket.md).
LocalPort may not subsequently be changed using `⎕WS`



If you specify a value of 0, the system will assign an available port number.
For example:
```apl
      'S1' ⎕wc'TCPSocket' ('LocalPort' 0)
      S1.LocalPort
4047
```



For a process that is completing a connection, LocalPort is allocated by the
system and is effectively read-only.


