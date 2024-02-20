




<h1 class="heading"><span class="name">TCPSend</span></h1>

Applies To: [TCPSocket](../a-z/tcpsocket.md)


**Description**


This method is used to send data to a remote process connected to a [TCPSocket](../a-z/tcpsocket.md) object


The argument to TCPSend is a 1 or 3-element array as follows:


| `[1]` | Data | the data to be sent |
| --- | --- | ---  |
| `[2]` | IP address | character vector |
| `[3]` | Port number | integer |


If Style is `'Char'`, the data to be sent must be a character vector. If Style is `'Raw'`, the data to be sent must be an integer vector whose elements are in the range -128 to 255. If Style is `'APL'`, any array may be transmitted.


The optional *IP address* and *Port number* parameters specify the intended recipient of the message and apply only if the [SocketType](../a-z/sockettype.md) is `'UDP'`, in which case they are mandatory. If the [SocketType](../a-z/sockettype.md) is `'Stream'`, these parameters will be ignored and should be omitted.



