# MMS
Documentation of the Met Messaging System, most of the documentation is on the Wiki (https://github.com/metno/MMS/wiki)

## Architecture (C4)

### Context
![Context diagram](http://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/metno/MMS/master/architecture/context.puml)

### Container
#### Production Hub
![Container diagram for Production Hub](http://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/metno/MMS/master/architecture/container.puml)

### Component
![Component diagram for MMS Daemon (mmsd)](http://www.plantuml.com/plantuml/proxy?src=https://raw.githubusercontent.com/metno/MMS/master/architecture/component.puml)

## MMS-clients

The main program is written in go, found at https://github.com/metno/go-mms.
Also under development is a python-client at  https://github.com/metno/py-mms.
