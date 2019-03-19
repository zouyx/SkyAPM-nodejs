# Install nodejs agent

## Installation nodejs module
Add the skyapm.js module as a dependency to your application:
> npm install skyapm.js@latest --save

## Initialization
It’s important that the agent is started before you require any other modules in your Node.js application. and you should
require and start the agent in your application’s main file.

```javascript
require('skyapm.js').start({
    // Application code is showed in sky-walking-ui. Suggestion: set an unique name for each application, one
    // application's nodes share the same code.
    // this value cannot be empty.
    serviceName: 'test',
    // Collector agent_gRPC/grpc service addresses.
    // default value: localhost:11800
    directServers: 'localhost:11800'
});

*NOTE*: If your application is using egg framework. please read the [deploy agent in egg framework](how-to-deploy-agent-in-egg-framework.md).
