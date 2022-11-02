




# AMOD-119 System context definition
##Concerns	
Visualise the system context after consolidation of the system functional scope.

##Viewpoint
In Capella this corresponds to a SAB diagram.

Mandatory viewpoint:

``` mermaid
classDiagram
direction TB 
class SystemContextDefinition 
<<viewpoint>> SystemContextDefinition
class SystemOfInterest
<<viewpointelement>> SystemOfInterest
class Actor
<<viewpointelement>> Actor

SystemContextDefinition "1" --o "1" SystemOfInterest
SystemContextDefinition "1" --o "1..*" Actor
Actor "1..*" -- "1" SystemOfInterest : Interacts with > 
```
**Diagram modelling rules**
(Link)TODO

**Element modelling rules**
(Link)TODO

**Viewpoint modelling rules**
[Viewpoint Rules AMOD-119](../system_analysis.md#amod-119-system-context-definition)