```mermaid
classDiagram
    FlowModule <-- ReactionModule
    FlowModule <-- AnalysisModule
    FlowModule <-- SubstrateEluentModule
    FlowChemistryProtocol *-- Author
    FlowChemistryProtocol *-- FlowModule
    FlowChemistryProtocol *-- InputParameter
    FlowChemistryProtocol *-- ResponseParameter
    FlowChemistryProtocol *-- ReactionModule
    FlowChemistryProtocol *-- AnalysisModule
    FlowChemistryProtocol *-- SubstrateEluentModule
    
    class FlowChemistryProtocol {
        +string description*
        +string title*
        +string subject*
        +Author[0..*] authors*
        +FlowModule[0..*] flowmodules*
        +InputParameter[0..*] inputparameters*
        +ResponseParameter[0..*] responseparameters*
        +ReactionModule[0..*] reaction_modules
        +AnalysisModule[0..*] analysis_modules
        +SubstrateEluentModule[0..*] substrate_eluent_modules
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
    }
    
    class ReactionModule {
    }
    
    class AnalysisModule {
    }
    
    class SubstrateEluentModule {
        +float molar_concentration
        +string description
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