




<h1 class="heading"><span class="name">LocalAddr</span></h1>
| Applies To: | [TCPSocket](../a-z/tcpsocket.md) |
| --- | ---  |

| Applies To: | [TCPSocket](../a-z/tcpsocket.md) | [TCPSocket](../a-z/tcpsocket.md) |  |  |
| --- | --- | ---  |
| [TCPSocket](../a-z/tcpsocket.md) |  |  |


Description


The LocalAddr property is a character vector that specifies the IP address of your computer. Its default value is `'0.0.0.0'`.


Unless your computer has more than one network adapter each identified by a different IP address, you do not need to specify LocalAddr. However, in this case you may use *either* LocalAddr *or*[ LocalAddrName](../a-z/localaddrname.md) to identify the adapter. If you specify both properties, the value of [LocalAddrName](../a-z/localaddrname.md) will be ignored.


Note that you may also set the value of LocalAddr to an empty character vector. In this case, the value returned by `⎕WG` will be `'0.0.0.0'`.


LocalAddr may only be specified in the `⎕WC` statement that creates the [TCPSocket](../a-z/tcpsocket.md) and may not subsequently be changed using `⎕WS`.



