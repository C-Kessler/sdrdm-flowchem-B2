```mermaid
classDiagram
    FlowChemistryProtocol *-- Author
    FlowChemistryProtocol *-- Flowmodule
    FlowChemistryProtocol *-- InputParameter
    FlowChemistryProtocol *-- ResponseParameter
    
    class FlowChemistryProtocol {
        +string description*
        +string title*
        +string subject*
        +Author[0..*] authors*
        +Flowmodule[0..*] flowmodules*
        +InputParameter[0..*] inputparameters*
        +ResponseParameter[0..*] responseparameters*
    }
    
    class Author {
        +string name*
        +string affiliation
    }
    
    class Flowmodule {
        +string key*
        +string id*
        +string manufacturer
    }
    
    class InputParameter {
        +string key*
        +string id*
        +float value*
    }
    
    class ResponseParameter {
        +string key*
        +float value*
    }
    
```