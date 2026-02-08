# Healthcare Clinical Ontology Project: Knowledge Representation Using OWL 2  


👤 AUTHOR
----------------------    
- **Bishozit Chandra Das**  
- Student ID: **VR544246**  
- MSc in **Artificial Intelligence** at Università degli Studi di Verona  
- [BishozitChandraDas](https://github.com/BishozitChandraDas)  


PROJECT DESCRIPTION
----------------------  
This project presents an advanced **Healthcare Clinical Ontology** developed using **OWL 2** and the **Protégé ontology editor**.  
The ontology models real-world healthcare concepts and their semantic relationships, enabling structured knowledge representation, interoperability, and logical reasoning.

The ontology covers core clinical entities such as patients, doctors, diseases, treatments, medications, appointments, hospitals, and medical records.  
It is designed for academic purposes and demonstrates the use of **classes, object properties, data properties, individuals, and reasoning** in the healthcare domain.


<img width="1024" height="768" alt="Overall Architecture of the Ontology Asserted Hierarchy" src="Overall%20architecture.jpeg" />  
Figure 1: Overall Architecture of the Ontology Asserted Hierarchy


PROJECT STRUCTURE
--------------------
1. Healthcare_Clinical_Ontology_2.0.owl  → Final OWL ontology file  

2. Project Report.pdf                   → Academic project report  

3. Overall architecture.jpeg            → Protégé asserted class hierarchy output  

4. README.md / readme.ad                → Project documentation  


ONTOLOGY DESIGN
--------------------
The ontology defines the following main concepts:

- **Person** (Superclass)  
  - Patient  
  - Doctor  
  - Nurse  

- Disease  
- Symptom  
- Diagnosis  
- Treatment  
- Medication  
- Prescription  
- Appointment  
- LabTest  
- MedicalRecord  
- Hospital  
- Department  
- Billing  

This class hierarchy ensures semantic clarity and reuse through inheritance.


OBJECT PROPERTIES
--------------------
The ontology includes the following object properties:

- `hasSymptom`        → Patient → Symptom  
- `diagnosedWith`     → Patient → Disease  
- `treatedBy`         → Patient → Doctor  
- `prescribes`        → Doctor → Medication  
- `undergoesTreatment`→ Patient → Treatment  
- `hasAppointment`    → Patient → Appointment  
- `storedIn`          → MedicalRecord → Hospital  

These properties define meaningful relationships between healthcare entities.


DATA PROPERTIES
--------------------
The following data properties are used:

- `patientID`     → Patient → string  
- `age`           → Person → integer  
- `gender`        → Person → string  
- `specialization`→ Doctor → string  
- `diseaseName`   → Disease → string  

Data properties allow the attachment of literal values to individuals.


INDIVIDUALS (INSTANCES)
------------------------
Example individuals included in the ontology:

- **JohnDoe** – Patient  
  - patientID: P1001  
  - age: 45  
  - gender: Male  

- **DrSmith** – Doctor  
  - specialization: Endocrinology  

- **Diabetes** – Disease  
- **Insulin** – Medication  
- **CityHospital** – Hospital  

These individuals demonstrate instantiation of abstract ontology classes.


HOW TO USE
-------------
1. Open **Protégé 5.x+**
2. Go to `File → Open`
3. Select `Healthcare_Clinical_Ontology_2.0.owl`
4. Explore:
   - Classes
   - Object Properties
   - Data Properties
   - Individuals

5. Run the reasoner:
   - `Reasoner → HermiT → Start Reasoner`


REASONING AND INFERENCE
------------------------
The ontology supports reasoning using OWL reasoners such as **HermiT**.

Reasoning enables:
- Automatic classification of individuals
- Detection of logical inconsistencies
- Inference of implicit subclass relationships

The asserted and inferred class hierarchies are consistent, confirming the correctness of the ontology.


USE CASES
-----------
- Clinical data integration
- Electronic Health Record (EHR) modeling
- Decision support systems
- Medical research and analytics
- Academic teaching of knowledge representation


LIMITATIONS
-------------
- No temporal modeling of disease progression
- Limited laboratory test representation
- No explicit security or privacy modeling
- No direct alignment with external medical standards


FUTURE ENHANCEMENTS
--------------------
- Integration of **SWRL rules** for clinical decision logic
- Mapping with standard ontologies (SNOMED CT, ICD-10)
- Extension with laboratory and imaging data
- Support for temporal and probabilistic reasoning


NOTES
--------
- The ontology is OWL 2 compliant
- Developed for academic and educational purposes
- Fully compatible with Protégé reasoners
