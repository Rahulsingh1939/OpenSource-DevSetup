# Data for the Common Good (D4CG)

Data for the Common Good (D4CG) is dedicated to building communities, platforms, and ecosystems that maximize the potential of data to drive discovery and improve human health. By leveraging collaborative efforts and advanced data analytics, D4CG aims to transform health data into actionable insights for the greater good.

## Key Initiatives

### Pediatric Cancer Data Commons (PCDC)

The PCDC is D4CG's flagship project, aggregating clinical data from pediatric, adolescent and young adult (AYA), and adult cancer patients worldwide. Utilizing the open-source Gen3 platform, the PCDC houses data on nearly 40,000 patients, providing a unified portal for researchers to explore and access diverse cancer data. :contentReference[oaicite:0]{index=0}

### GEARBOx

Developed in partnership with The Leukemia & Lymphoma Society, GEARBOx is a decision-support tool that matches patients to potential clinical trials based on their clinical and genomic profiles, as well as trial protocol information. Initially designed for acute myeloid leukemia patients, GEARBOx is being expanded to accommodate other cancer types.

### mCODE (Minimal Common Oncology Data Elements)

mCODE is an initiative aimed at enhancing interoperability by establishing a core set of structured data elements for oncology electronic health records (EHRs). This standardized approach facilitates consistent data collection and sharing, improving cancer care quality. :contentReference[oaicite:1]{index=1}

## Additional Resources

- **Integrated Trial Matching for Cancer Patients and Providers**: This resource discusses the integration of trial matching services within EHR systems, enhancing accessibility to clinical trials for patients and providers.

- **Matching Services**: An overview of various services designed to connect patients with appropriate clinical trials, emphasizing the importance of personalized treatment options.

## Learn More

For more information about D4CG and its initiatives, visit the official website: :
https://www.hl7.org/fhir/us/mcode/

https://confluence.hl7.org/spaces/COD/pages/66938394/Integrated+Trial+Matching+for+Cancer+Patients+and+Providers

Github: 
https://github.com/mcode/clinical-trial-matching-service

https://gearbox.pedscommons.org/

https://github.com/chicagopcdc/gearbox-matching


# Project 6: Developing a Translation Service to Connect GEARBOx API with mCODE Trial Matching Service

## Description
This project aims to build a translation service that connects the **GEARBOx API** with the **mCODE** (Minimal Common Oncology Data Elements) trial matching service. The goal is to enable seamless translation of oncology data between **GEARBOx** and **mCODE**, allowing healthcare providers, researchers, and clinical trial platforms to effectively match patients to relevant clinical trials based on their mCODE-compliant health data.

## Expected Outcomes
- **Data Mapping & Transformation**
- **Interoperability & Validation**

## Skills
- **Python**
- **Typescript**

## Mentors
TBD - One of the Senior Developers in the team.

## Project Size
- **350 hours**

## Rating
- **Medium**


# Procedure : 
That sounds like an exciting GSoC project! Here’s how you can approach it:

### **1. Understand the Project Scope**
- The goal is to **build a translation service** between **GEARBOx API** and **mCODE trial matching service**.
- You need to **convert oncology data** from one format to another so that trial-matching works efficiently.

### **2. Required Skills**
- **Python & TypeScript**: You need backend (Python) and potentially frontend/service interaction skills (TypeScript).
- **API Integration**: You will likely work with RESTful or GraphQL APIs.
- **FHIR Standard (HL7 mCODE)**: Since mCODE follows FHIR (Fast Healthcare Interoperability Resources), you should get familiar with it.
- **Data Mapping & Validation**: You’ll translate data formats, ensuring the integrity of patient and trial data.

### **3. Steps to Get Started**
#### **(A) Learn About the Technologies**
1. **FHIR & mCODE**
   - Read about **FHIR (HL7)**: [https://www.hl7.org/fhir/](https://www.hl7.org/fhir/)
   - Check out **mCODE documentation**: [https://www.hl7.org/fhir/us/mcode/](https://www.hl7.org/fhir/us/mcode/)

2. **GEARBOx API**
   - Explore the **GEARBOx matching service**: [https://github.com/chicagopcdc/gearbox-matching](https://github.com/chicagopcdc/gearbox-matching)
   - Try making sample API calls if possible.

3. **Clinical Trial Matching**
   - Read how trial matching services work: [https://confluence.hl7.org/spaces/COD/pages/66938394/Integrated+Trial+Matching+for+Cancer+Patients+and+Providers](https://confluence.hl7.org/spaces/COD/pages/66938394/Integrated+Trial+Matching+for+Cancer+Patients+and+Providers)

#### **(B) Start Hands-On Practice**
1. **Experiment with API calls**
   - Use **Postman** or Python’s `requests` library to explore the GEARBOx API.
   - Try to map mCODE FHIR data to what GEARBOx needs.

2. **Work on a Small Prototype**
   - Write a Python script that takes **mCODE format patient data** and converts it into a format accepted by **GEARBOx API**.

3. **Look into JSON Schema & Data Transformation**
   - Learn how **mCODE structures patient data** (JSON format).
   - Understand how **GEARBOx accepts input data**.

#### **(C) Contribute & Connect**
- **Join Discussions**: Check if the project has a Slack/Discord/GitHub Discussions.
- **Look for “Good First Issues”** on GitHub.
- **Engage with the Community**: Ask about the best ways to contribute.

### **4. Proposal Writing Tips**
- Explain **why you’re interested** in this project.
- Show understanding of **FHIR/mCODE & API integration**.
- Outline **a simple plan** (break it into milestones).
- Mention **any related projects** or API work you’ve done.

---
