# Patient Intake Form Automation (n8n Dummy Project)

## Overview
This dummy n8n project demonstrates an automated workflow for processing new patient intake forms. In a real-world scenario, this would involve automatically extracting submitted data and inputting it into an Electronic Health Record (EHR) system, significantly reducing manual data entry and potential errors.

## Problem Addressed
Manual processing of patient intake forms (whether paper or digital) is time-consuming, prone to human error, and delays patient onboarding. Clinics often spend significant hours on this administrative task.

## n8n Solution
This n8n workflow is designed to:
1.  **Receive Form Submissions:** Simulate receiving data from a new patient intake form (e.g., via a Webhook or by reading from a dummy file).
2.  **Extract & Transform Data:** Parse the incoming data, validate fields, and format it for an EHR system.
3.  **Simulate EHR Integration:** Demonstrate how the processed data would be sent to a mock EHR system (e.g., via an HTTP Request to a placeholder API).

## Workflow Description
The core of this automation involves:
* **Webhook Trigger Node:** To simulate receiving new form submissions (or a dummy data source for testing).
* **Edit Fields (Set) Node:** To normalize and prepare the incoming data.
* **Code Node:** For any complex data transformations, validation, or conditional logic.
* **HTTP Request Node:** To simulate sending the processed data to a dummy EHR API endpoint. In a real setup, this would integrate with a specific EHR API (e.g., Epic, Cerner, or a custom internal system).

## Setup for Dummy Project
To run this dummy project in your n8n instance:
1.  **Import the workflow:** Download `patient_intake_workflow.json` from this folder and import it into your n8n instance.
2.  **Dummy Data:** The workflow will use a `Webhook` to simulate incoming form data. You can test this by sending a sample JSON payload to the Webhook URL (provided by the n8n Webhook node). A `dummy_intake_form_payload.json` file is provided for this purpose.

## Files in This Folder
* `README.md`: This file.
* `patient_intake_workflow.json`: The exported n8n workflow for patient intake form automation.
* `data/dummy_intake_form_payload.json`: A sample JSON payload representing a submitted patient intake form.

## Future Enhancements
* Integration with actual form builders (e.g., Typeform, Google Forms, custom web forms).
* Robust error handling for invalid or missing data.
* Lookup and update existing patient records instead of always creating new ones.
* Notifications for successful processing or errors.
