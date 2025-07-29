# Medication Refill Request Processing (n8n Dummy Project)

## Overview
This dummy n8n project demonstrates an automated workflow for the initial screening and routing of medication refill requests. The goal is to streamline the process, reduce manual workload on nurses and administrative staff, and potentially speed up patient response times.

## Problem Addressed
Clinics often receive numerous medication refill requests via phone, patient portals, or faxes. Manually triaging these requests to determine if they are straightforward refills or require physician review can be time-consuming and inefficient.

## n8n Solution
This n8n workflow is designed to:
1.  **Receive Refill Requests:** Simulate receiving medication refill requests (e.g., via a Webhook from a patient portal or an email parsing service).
2.  **Screen Requests:** Automatically check for common criteria (e.g., simple refill vs. complex request requiring physician approval, last doctor visit date).
3.  **Route Requests:** Direct requests to appropriate "teams" or systems based on screening results (e.g., "straightforward refills" to pharmacy/admin team, "complex cases" to physician's queue).
4.  **Simulate Notifications:** Send mock notifications or log the action taken.

## Workflow Description
The core of this automation involves:
* **Webhook Trigger Node:** To simulate receiving new refill requests.
* **Edit Fields (Set) Node:** To normalize and prepare the incoming request data.
* **Code Node:** For custom logic to evaluate refill complexity (e.g., checking medication type, last fill date, or patient history flags).
* **Switch Node:** To route the request down different paths based on the evaluation from the Code node (e.g., "Simple Refill" vs. "Requires Review").
* **HTTP Request Node(s):** To simulate sending the request to different internal systems or sending notifications (e.g., a "Simple Refill API" or "Physician Review Queue").

## Setup for Dummy Project
To run this dummy project in your n8n instance:
1.  **Import the workflow:** Download `medication_refill_workflow.json` from this folder and import it into your n8n instance.
2.  **Dummy Data:** The workflow uses a `Webhook` to simulate incoming refill requests. You can test this by sending sample JSON payloads to the Webhook URL. `data/dummy_refill_request_simple.json` and `data/dummy_refill_request_complex.json` are provided for testing different routing paths.

## Files in This Folder
* `README.md`: This file.
* `medication_refill_workflow.json`: The exported n8n workflow for medication refill processing.
* `data/dummy_refill_request_simple.json`: A sample JSON payload for a simple refill request.
* `data/dummy_refill_request_complex.json`: A sample JSON payload for a complex refill request.

## Future Enhancements
* Integration with actual patient portals, EHR systems, or pharmacy dispensing systems.
* Automated communication with patients (e.g., "your refill is being processed").
* Integration with AI/NLP for more nuanced request screening.
* Logging all requests and actions in a central database.
