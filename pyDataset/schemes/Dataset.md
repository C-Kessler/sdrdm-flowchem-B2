```mermaid
classDiagram
    FlowChemistryProtocol *-- Author
    FlowChemistryProtocol *-- Parameter
    FlowChemistryProtocol *-- Flowmodule
    
    class FlowChemistryProtocol {
        +string description*
        +string title*
        +string subject*
        +Author[0..*] authors*
        +Parameter[0..*] parameters*
        +Flowmodule[0..*] flowmodules*
    }
    
    class Author {
        +string name*
        +string affiliation
    }
    
    class Parameter {
        +string key*
        +float value*
    }
    
    class Flowmodule {
        +string key*
        +float value*
    }
    
```