Dataset-BCO
========================

### BCO_Spec_V1.2
-----------------
The Dataset BCO was developed with the [Data integration use case](https://github.com/biocompute-objects/BCO_Spec_V1.2/blob/master/BCO_Spec_V1.2.md#data-integration-use-case) in mind. 

* A BCO can be used to provide clarity and transparency of the data integration process to both the new and existing collaborators. When new data is integrated into the existing data model, BCO can be used to describe data source information (eg- authors/contributors, data version etc), a QC workflow, data content, data modification if any. The BCO also allows reuse of the same workflow to integrate new data with same structure and source. BCO also provides a way to access and track data records which were eliminated in the integration/QC process due to rules or restrictions of the existing data model. Knowledgebases using BCOs in the form of ‘readme’ can provide provenance for every piece of data that is collected and presented to the user. Such granular tracking facilitates fair sharing of data and provides mechanisms for adherence to licensing requirements associated with specific datasets.

The Dataset BCO is derived and developed from [v1.2](https://github.com/biocompute-objects/BCO_Specification/releases/tag/v1.2) and is compliant with the BCO framework. The dataset BCO has been developed as a 'readme' for a dataset upon integration into a knowledgebase. The Dataset BCO includes:

* Provenance information about the dataset
* License information about the data and the scripts
* Usability domain, searchable keywords
* Pipeline steps that include scripts and extensive description
* Information about the script that includes the script name, type and location
* Input and output files involved in the dataset creation that also includes source files and log files
* Column headers and descriptions of the dataset file 
* Statistics for the dataset

### User Guide
--------------
The dataset BCO is created by implementing the BCO Specifications (v1.2) which is based on the fundamentals of datatyping. The details to define DatasetBCO are found in [primitives.json] and [base_typeDatasetBCO.json](https://github.com/biocompute-objects/Dataset-BCO/blob/master/base_typeDatasetBCO.json) .All Dataset BCO types must inherit from the [base_typeDatasetBCO.json](https://github.com/biocompute-objects/Dataset-BCO/blob/master/base_typeDatasetBCO.json) that is complaint with the BCO framework. The dataset BCO is in JSON format, the format that is both machine and human readable. Thus a parser can be written to parse the json to display or create all or only the required fields in txt format. The dataset BCO in text format can be used as a readme for the dataset. An example Dataset BCO [Dataset_BCO_example](https://github.com/biocompute-objects/Dataset-BCO/blob/master/Dataset_BCO_example) has been uploaded in JSON format for better understanding. 

For more information on the BioCompute Objects please see the links -
* BioComputeObject Website: https://biocomputeobject.org/
* GitHub repository for BioCompute Objects: https://github.com/biocompute-objects/
* Current BCO specification (v1.2): https://github.com/biocompute-objects/BCO_Specification/blob/v1.2/BCO_Spec_V1.2.pdf

