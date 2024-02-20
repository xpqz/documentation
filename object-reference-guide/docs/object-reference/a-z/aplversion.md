




<h1 class="heading"><span class="name">APLVersion</span></h1>

Applies To: [Root](./root.md)


**Description**


This is a read-only property that provides information about the Version of Dyalog APL that you are using. It is
a 4-element vector of character vectors as described in the table below. In future releases these values may change, be removed, or new ones added.


| Index | Description | Possible Values |
| --- | --- | ---  |
| `[1]` | Target Environment | `Windows Windows-64 Windows Mobile Linux Linux-64 AIX AIX-64 Mac-64 Solaris Solaris-64` |
| `[2]` | Version Number |  |
| `[3]` | Version Type | W Windows S Server (terminal) version M Motif P PocketAPL | W | Windows | S | Server (terminal) version | M | Motif | P | PocketAPL |
| W | Windows |
| S | Server (terminal) version |
| M | Motif |
| P | PocketAPL |
| `[4]` | Program Type | `Development Runtime DLL DLLRT` |

#### Example
```apl
      '.'⎕WG'APLVersion'
┌──────────┬────────────┬─┬───────────┐
│Windows-64│18.0.38434.0│W│Development│
└──────────┴────────────┴─┴───────────┘

```



