# Dataset

This is the place where you can describe the complete module/dataset and give information about all the details. Markdown offers a convenient way to enable as much space as needed to elucidate purpose and capabilities of your data model.

### FlowChemistryProtocol

This is the root of the data model and contains all objects defined in this example. While its good practice to have a single root, you can define as many roots as you like. Furthermore, the name does not have to be ```Root``` and can be any other name.

- __description*__
  - Type: string
  - Description: Describes the content of the dataset.
  - Dataverse: pyDaRUS.Citation.description.text
- __title*__
  - Type: string
  - Description: Title of the work
  - Dataverse: pyDaRUS.Citation.title
- __subject*__
  - Type: string
  - Description: Subject of matter linked to the dataset
  - Dataverse: pyDaRUS.Citation.subject
- __authors*__
  - Type: Author
  - Multiple: True
  - Description: Authors of this dataset.
- __flowmodules*__
  - Type: FlowModule
  - Multiple: True
  - Description: Equipment used in the flowprocess

### Author

This is another object that represents the author of the dataset. Please note, that the options here contain all required fields but also custom ones. In this example, the ```Dataverse``` option specifies where each field should be mapped, when exported to a Dataverse format. Hence, these options allow you to link your dataset towards any other data model without writing code by yourself.

- __name*__
  - Type: string
  - Description: Full name including given and family name
  - Dataverse: pyDaRUS.Citation.author.name
- __affiliation__
  - Type: string
  - Description: To which organization the author is affiliated to
  - Dataverse: pyDaRUS.Citation.author.affiliation
  
### FlowModule

This section should provide all details about the equipment of the setup.

- __key*__
  - Type: string
  - Description: Name of the flow module
  - Dataverse: pyDaRUS.Process.method_parameters.name
- __id*__
  - Type: string
  - Description: A unique id that should be findable in the flow scheme
  - Dataverse: pyDaRUS.Process.method_parameters.value
- __manufacturer__
  - Type: string
  - Description: Name of the manufacturer of the device
- __typenumber__
  - Type: string
  - Description: Exact type number given by the manufacturer of the device
  - Dataverse: pyDaRUS.Process.method_parameters.value
- __series__
  - Type: string
  - Description: The Series of the device
  - Dataverse: pyDaRUS.Process.method_parameters.value
- __manuallink__
  - Type: string
  - Description: Possibility to get the manual of the device
  - Dataverse: pyDaRUS.Process.method_parameters.value

### ReactionModule [_FlowModule_]

This section should provide all details about the equipment of the setup.

- __test*__
  - Type: string
  - Description: Name of the flow module
  - Dataverse: pyDaRUS.Process.method_parameters.name

### AnalysisModule [_FlowModule_]

This section should provide all details about the equipment of the setup.

- __test*__
  - Type: string
  - Description: Name of the flow module
  - Dataverse: pyDaRUS.Process.method_parameters.name

### SubstrateEluentModule [_FlowModule_]

This section should provide all details about the equipment of the setup.

- __molarconcentration__
  - Type: float
  - Description: Molar concentration (molar)
  - Dataverse: pyDaRUS.Process.method_parameters.value
- __description__
  - Type: string
  - Description: Name the components
  - Dataverse: pyDaRUS.Process.method_parameters.name

### Randomstuff 

This section should provide all details about the equipment of the setup.

- __molarconcentration__
  - Type: float
  - Description: Molar concentration (molar)
  - Dataverse: pyDaRUS.Process.method_parameters.value
- __description__
  - Type: string
  - Description: Name the components
  - Dataverse: pyDaRUS.Process.method_parameters.name
