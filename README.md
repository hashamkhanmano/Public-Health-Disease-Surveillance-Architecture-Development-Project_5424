# Public-Health-Disease-Surveillance-Architecture-Development-Project_5424
This is a comprehensive, professional README.md file that weaves all five parts of your architecture development into a single, cohesive project. It is structured to guide a viewer through the initial setup all the way to the final data exchange.

🏥 UP-HIE: Regional Healthcare Architecture & Outbreak Surveillance
A 5-Part Implementation of a Health Information Exchange (HIE) Network.

This repository documents the development of a baseline healthcare architecture designed to simulate a regional Health Information Exchange (HIE). The project connects four virtual hospitals to a central exchange hub (UPHIE) to demonstrate real-time syndromic surveillance and interoperability using modern healthcare standards.

🗺️ Project Architecture
The environment consists of five distinct Virtual Machines (VMs) serving specific roles in the Michigan Upper Peninsula healthcare ecosystem:

UPHIE Hub: The central HAPI-FHIR server.

Aspirus Hospital: Regional node running OpenEMR.

Portage Health Hospital: Regional node running OpenEMR.

BCMH (Baraga County): Regional node running OpenEMR.

MGH (Marquette General): Regional node running OpenEMR.

🛠️ The Five-Part Development Lifecycle
Part 1: VM Configuration & Networking
Objective: Establish the hardware-level baseline.

Action: Configured 5 VMs with static IP addressing on a shared virtual subnet.

Validation: Connectivity verified via cross-node ping tests to ensure the "Hospitals" can reach the "Exchange."

Part 2: OpenEMR Installation & Security
Objective: Deploy Electronic Health Record (EHR) systems.

Action: Installed the LAMP stack and OpenEMR on all four hospital nodes.

Security: Implemented security hardening including restricted file permissions and database access controls to safeguard simulated patient data.

Part 3: Synthetic Data Generation (Synthea)
Objective: Populate the network with realistic, non-PII patient data.

Action: Used Synthea to generate synthetic patient histories, demographics, and clinical observations.

Simulation: Injected specific disease modules to simulate a regional outbreak (syndromic data) for testing surveillance capabilities.

Part 4: HAPI-FHIR Server Deployment
Objective: Establish a standardized interoperability hub.

Action: Configured a HAPI-FHIR server on the UPHIE VM.

Role: Acts as the central repository using the FHIR R4 standard, allowing disparate systems to communicate securely via a web-based REST API.

Part 5: Interoperability & Data Exchange
Objective: Demonstrate real-time public health surveillance.

Action: Executed FHIR message exchanges where hospitals POST data to the UPHIE hub.

Analytics: Utilized scripts to parse FHIR resources, identifying disease trends and "spikes" in symptoms to inform public health policy and resource allocation.

🚀 Technical Stack
Virtualization: VMware / VirtualBox

EHR Platform: OpenEMR (PHP/MySQL)

Interoperability: HAPI-FHIR (Java)

Data Generation: Synthea (Java)

Standards: HL7 FHIR (Fast Healthcare Interoperability Resources)

📈 Public Health Impact
By utilizing this architecture, public health agencies can:

Detect: Identify outbreaks in near real-time through syndromic data.

Respond: Coordinate faster response times among regional healthcare stakeholders.

Inform: Create evidence-based policies based on aggregated, standardized data trends.

📜 License
This project is for educational and simulation purposes. All patient data generated is synthetic and does not represent real individuals.
Public Health Disease Surveillance Architecture Development Project
