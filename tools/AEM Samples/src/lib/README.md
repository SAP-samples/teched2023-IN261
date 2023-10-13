# Solace JavaScript Messaging API
*Copyright 2011-2022 Solace Corporation. All rights reserved.*

This software is proprietary software of Solace Corporation and intended only
for use in conjunction with one or more Solace Message Routers.  By using this
software, you are agreeing to the license terms and conditions located at
https://solace.com/license-software.


## INTRODUCTION
This is the Solace JavaScript Messaging API. This API
allows JavaScript browser and mobile applications to send and receive
messages to and from a Solace Messaging Router.

## PACKAGING
A zip package is included with this distribution. The file is named 
`solclientjs-<version>.zip` and includes:
* `/lib`                    JavaScript module files
* `/docs`                   API online docs		

## SAMPLES
Tutorials and samples with detailed instructions how to run them, are
available on GitHub from the following location: 
[Solace Samples: JavaScript](https://github.com/SolaceSamples/solace-samples-javascript)

## API VARIATIONS
There are different variations of the API that can be used. The differences
between them include available logging verbosity and whether or not the API
has been minified.

When the available logging verbosity has been reduced, this is done to
improve the performance the application but this reduces the ability to
debug problems.

Minified libraries are both smaller and optimized for performance. However,
this comes at the expense of making debugging more difficult.

The following table summarizes the available API variations:

    | Variation  | Minified | Available Logs           |
    -------------|----------|---------------------------
    | Debug      | No       | All                      |
    | Full       | No       | INFO, WARN, ERROR, FATAL |
    | Production | Yes      | INFO, WARN, ERROR, FATAL |

To load an API variation, use one of the following statements:

    <head>
        <script src="solclient.js"></script>       <!-- production -->
    OR  <script src="solclient-full.js"></script>  <!-- full       -->
    OR  <script src="solclient-debug.js"></script> <!-- debug      -->
    </head>
          
## API PROFILES
The API has the concept of an initialization profile. The intent of the
profile is to allow old applications to remain compatible with old versions
of the API, while allowing new users to take advantage of new recommended
defaults.

When writing a new application, it is recommended to choose the newest
factory profile. For example, if `version10` is the newest available factory
profile, this snippet demonstrates how to initialize the API:
    
    var factoryProps = new solace.SolclientFactoryProperties();
    factoryProps.profile = solace.SolclientFactoryProfiles.version10;
    solace.SolclientFactory.init(factoryProps);

For backwards compatibility with applications written before the concept of
API profiles were introduced, the default profile is `version7`.

__IMPORTANT__: `solace.SolclientFactory.init` should be called before any other API
function is invoked.
    
## LOGGING
The default log level of the API is `INFO`.  If you want to change the log
level, use the `solace.SolclientFactory#setLogLevel` method after calling
`solace.SolclientFactory#init`.
    
The following snippet shows how to load the debug API, select the `version10`
API profile, and set the log level to `TRACE`, the most verbose log level:

    <head>
        <script src="solclient-debug.js"></script>
        <script type="text/javascript">
            var properties = new solace.SolclientFactoryProperties();
            properties.profile = solace.SolclientFactoryProfiles.version10;
            solace.SolclientFactory.init(properties);
            solace.SolclientFactory.setLogLevel(solace.LogLevel.TRACE);
        </script>
    </head>
