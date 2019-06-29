# oberbaum
Connect things in flexible ways using a simple config system
<img src=design.svg>
[edit this diagram](https://mermaidjs.github.io/mermaid-live-editor/#/edit/eyJjb2RlIjoiXG5cbmdyYXBoIExSXG4gIHN1YmdyYXBoXG4gICBZKDxiPmNvcmU8L2I-KVxuIGluaXQgLS0-IFpbXCJxdWVyeSBlbmRwb2ludHNcIl1cbiBaIC0tPiBaMVtyb3V0ZSBvdXRwdXQgYW5kIGV4ZWN1dGUgbWlkZGxld2FyZV0gXG5aMSAtLT4gWjJ7bmV3IHF1ZXJ5IHJlcXVpcmVkfVxuWjIgLS0geWVzIC0tPiBaXG5aMiAtLSBubyAtLT4gWjEgXG5cbiAgZW5kXG4gIHN1YmdyYXBoXG4gICBYKDxiPmNvbmZpZzwvYj4pIC0uLT4gaW5pdFxuICAgQShlbmRwb2ludHMpXG4gICBCKG1pZGRsZXdhcmUpXG4gICBDKHJvdXRpbmcpXG4gICBYIC0tLSBBXG4gICBYIC0tLSBCXG4gICBYIC0tLSBDXG4gIGVuZFxuICBzdWJncmFwaFxuIEEyKDxiPmVuZHBvaW50PC9iPilcbnBhcmFtZXRlcnMgLS0-IEQxKGVuY29kZXI_KVxuRDEgLS0-IHRyYW5zcG9ydFxudHJhbnNwb3J0IC0tPiBEMlxuIEQyKFwicGFyc2VyL2RlY29kZXI_XCIpIC0tPiByZXN1bHRcbiAgZW5kXG4gIHN1YmdyYXBoXG5CMig8Yj5taWRkbGV3YXJlPC9iPilcbmlucHV0IC0tPiBEMyh0cmFuc2Zvcm0pXG5EMyAtLT4gb3V0cHV0XG4gIGVuZFxuICBzdWJncmFwaFxuQzIoPGI-cm91dGU8L2I-KVxuRDRbXCJpbnB1dChzKVwiXSAtLT5cbkQ1W1wib3V0cHV0KHMpXCJdXG4gIGVuZFxuY2xhc3NEZWYgbGFiZWwgZmlsbDojZWVmLCBzdHJva2U6I2VlZlxuY2xhc3MgQTIsQjIsQzIsWCxZIGxhYmVsXG5BIC0uLSBBMlxuQiAtLi0gQjJcbkMgLS4tIEMyXG4iLCJtZXJtYWlkIjp7InRoZW1lIjoiZGVmYXVsdCJ9fQ)

## Everything is a Route
Routes have sets of inputs and outputs, and may optionally perform some processing on or with their inputs.
The config defines the initial inputs to the system and the connections between routes.

Middleware is a type of route that performs some processing.
An Endpoint is a type of middleware that connects to external resources.

## TODO/Short Term Goals
 * [ ] simple acyclical routing and example middleware - just process data.
 * [ ] route manager for loops and stuff - process data persistently.
 * [ ] config parser that talks to route manager - make it easy to process data.
 * [ ] implement jsonrpc endpoints for parity-ethereum - make it easy to process ethereum.
 * [ ] some non-trivial interaction between two nodes.
 * [ ] do everything [`parity-bridge`](https://github.com/paritytech/parity-bridge) currently does.
 * [ ] parse parts of configs provided directly by endpoints - make it meta.
 * [ ] offload middleware tasks to other software using endpoints - everything is pluggable.

## Roadmap/Long Term Goals
 * [ ] Port `parity-bridge` to simple middleware; port it's jsonrpc client logic to simple endpoints.
 * [ ] Implement endpoints for substrate chains; implement a substrate module that works with `parity-bridge` middleware.
 * [ ] Implement a substrate-ethereum bridge.
 * [ ] Do crazy things this isn't designed for.
