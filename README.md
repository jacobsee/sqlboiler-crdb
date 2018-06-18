# sqlboiler-crdb

## Installation

Installation is simple, just use go get. Once the binary is in your path sqlboiler will be able to use it if you run it with the driver name `crdb`.
```
# Install sqlboiler crdb driver
go get -u github.com/glerchundi/sqlboiler-crdb
# Generate models
sqlboiler crdb
```
It's configuration keys in sqlboiler are simple:
```
[crdb]
user="root"
pass=""
host="localhost"
port=26257
dbname="mydatabase"
sslmode="disable"
```

**Note**: Code generation against secure clusters is not tested yet.

## Development

This does use go-bindata to embed templates into the binary. You can run go-generate in the driver folder to re-gen the bindata after modifying templates. Other than that go build should be able to be used to build the binary.
