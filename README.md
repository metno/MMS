# MMS
Documentation of the Met Messaging System. Most of the documentation is on the Wiki (https://github.com/metno/MMS/wiki)

## Terminology
### Production hub
A unit that has the capacity to run custom code to process data and provide metadata, metrics and emits messages about events. An example is an instance of ecFlow accompanied by
an mmsd (MMS daemon).

### mmsd
A process providing metadata about the production hub it represents.

## Architecture (C4)

### Context
![Context diagram](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/metno/MMS/master/architecture/context.puml)

### Container
#### Production Hub
![Container diagram for Production Hub](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/metno/MMS/master/architecture/container.puml)

### Component
![Component diagram for MMS Daemon (mmsd)](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/metno/MMS/master/architecture/component.puml)

### Code
#### Client App
![Code diagram for Client App](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/metno/MMS/master/architecture/code_client.puml)

## MMS clients

The main program is written in Go, found at https://github.com/metno/go-mms.
Also under development is a Python client at https://github.com/metno/py-mms.
