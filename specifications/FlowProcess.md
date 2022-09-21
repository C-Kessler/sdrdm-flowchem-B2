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
- __parameters*__
  - Type: Parameter
  - Multiple: True
  - Description: Parameters to start and configure some process
- __flowmodules*__
  - Type: Flowmodule
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
  
### Parameter

This is another object used to describe the parameters of given dataset. As a final note, it is important to use the description of an object to its fullest. As you might noticed, the space in between the object definition ```###``` can be freely used to describe what this object is actually about. Ultimately, this gives you the opportunity to ensure users completely understand what the intention and use case of this object is in a readable way.

- __key*__
  - Type: string
  - Description: Name of the parameter
  - Dataverse: pyDaRUS.Process.method_parameters.name
- __value*__
  - Type: float
  - Description: Respective value of a parameter
  - Dataverse: pyDaRUS.Process.method_parameters.value

### Flowmodule

just a short text.

- __key*__
  - Type: string
  - Description: Name of the parameter
  - Dataverse: pyDaRUS.Process.method_parameters.name
- __value*__
  - Type: float
  - Description: Respective value of a parameter
  - Dataverse: pyDaRUS.Process.method_parameters.value