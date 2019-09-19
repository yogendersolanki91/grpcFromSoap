SOAP to GRPC Generator
==========================

This script generates Proto files from WSDL for a SOAP Service.

WSDL -> PROTO3 GRPC


What it can do
* Supports namespace to package generator.
* Can specify binding you want to convert.
* Generate the service and all the message in the WSDL.
* Supports Enum (Can create enums but can't enumrate all the field, issue with zeep)


What it can't do
Because feature of both framework cannot be mapped one to one, it won't give you final output that can be consumed direcly without couple of manual changes in the generated GRPC.

Following things need to be resolved manually.

* Nested namespace are not supported. (Recursive imports not supported in protobuf)
* Keywords conflict with generated code protobuf (Observed with GRPC C++  generator eg. howmany?).

