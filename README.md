# provViz

provViz is a simple tool that allows the user to visualize a provenance
graph collected by rdt or rdtLite using DDG Explorer.

To use it, call the prov.visualize function:
```
prov.visualize <- function (r.script.path = NULL, tool = "rdtLite")
```

## Parameters
**r.script.path** - The path to an R script.  This script will be 
executed with provenance captured by rdt or rdtLite.  If r.script.path
is NULL, the last provenance graph captured will be displayed.

**tool** - which tool to use to capture proveannce.  Possible values are "rdtLite" or "rdt".

## Known problems
If the user calls this with NULL for r.script.path but no provenance
has been captured yet in the session, there is a json string returned
but it is not valid.
