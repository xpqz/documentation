# Files Installed with Dyalog

### NET Interface Components

The components used to support the .NET interface are summarised below. Different versions of each component are supplied  according to the target platform.

- The Bridge DLL. This is the interface library through which all calls between Dyalog APL and the .NET Framework are processed
- The DyalogProvider DLL. This DLL performs the initial processing of an `APLScript`.
- The *APLScript* Compiler. This is itself  written in Dyalog APL and packaged as an executable.
- The DyalogNet DLL; a subsidiary library
- The Dyalog DLL. This is the engine that executes all APL code that is hosted by and called from another .NET application.

For a list of the files associated with each of these components, see 

Files and Directories

Files on page 1
.

### Code Samples

The `samples` subdirectory contains several sub-directories relating to the .NET interface:

- `aplclasses`; a sub-directory that contains examples of .NET classes written in APL.
- `aplscript`; a sub-directory that contains APLScript examples.
- `asp.net`; a sub-directory that is mapped to the IIS Virtual Directory `dyalog.net`, and contains various sample APL Web applications.
- `winforms`; a sub-directory that contains sample applications that use the `System.Windows.Forms` GUI classes.
- `web.config`: this file specifies Dyalog configuration parameters for ASP.NET. See The web.config file on page 1.
