




<h1 class="heading"><span class="name">GetBuildID</span></h1>
| Applies To: | [Root](../a-z/root.md) |
| --- | ---  |

| Applies To: | [Root](../a-z/root.md) | [Root](../a-z/root.md) |  |  |
| --- | --- | ---  |
| [Root](../a-z/root.md) |  |  |


Description


This method is used to obtain the Build ID of a Dyalog executable or the checksum of a file.




The argument to GetBuildID is `⍬` or a
single item as follows:

| `[1]` | File name | character vector |
| --- | --- | ---  |



The (shy) result is an 8-element character vector of hexadecimal digits that
represents the Build ID.


If the argument is `⍬`, the build id is
that of the current version of Dyalog that is running the expression.


Note that although this method is designed to uniquely identify different
versions of Dyalog by its checksum, it may be used to obtain a checksum
for *any* arbitrary file.

#### Examples:
```apl
      GetBuildID ⍬
38091b76
      GetBuildID 'E:\DYALOG81\DYALOG.EXE'
cbf0d376
      GetBuildID 'myfile'
4a29334d
```


Note that if the file does not exist, the result is 00000000.


