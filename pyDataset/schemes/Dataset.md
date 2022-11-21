```mermaid
classDiagram
    FlowModule <-- ReactionModule
    FlowModule <-- AnalysisModule
    FlowModule <-- SubstrateEluentModule
    FlowChemistryProtocol *-- Author
    FlowChemistryProtocol *-- FlowModule
    
    class FlowChemistryProtocol {
        +string description*
        +string title*
        +string subject*
        +Author[0..*] authors*
        +FlowModule[0..*] flowmodules*
    }
    
    class Author {
        +string name*
        +string affiliation
    }
    
    class FlowModule {
        +string key*
        +string id*
        +string manufacturer
        +string typenumber
        +string series
        +string manuallink
    }
    
    class ReactionModule {
        +string test*
    }
    
    class AnalysisModule {
        +string test*
    }
    
    class SubstrateEluentModule {
        +float molarconcentration
        +string description
    }
    
```