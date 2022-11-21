```mermaid
classDiagram
    FlowModule <-- ReactionModule
    FlowModule <-- AnalysisModule
    FlowModule <-- SubstrateEluentModule
    FlowChemistryProtocol *-- Author
    FlowChemistryProtocol *-- FlowModule
    FlowModule *-- ReactionModule
    FlowModule *-- AnalysisModule
    FlowModule *-- SubstrateEluentModule
    
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
        +string type_number
        +string series
        +string manual_link
        +ReactionModule[0..*] reactionmodules
        +AnalysisModule[0..*] analysismodules
        +SubstrateEluentModule[0..*] substrateeluentmodules
    }
    
    class ReactionModule {
    }
    
    class AnalysisModule {
    }
    
    class SubstrateEluentModule {
        +float molar_concentration
        +string description
    }
    
```