# Automated Appointment Reminders (n8n Dummy Project)

## Overview
This dummy n8n project demonstrates an automated workflow for sending appointment reminders to patients. In a real-world scenario, this would help reduce no-show rates and improve clinic efficiency.

## Problem Addressed
Clinics often face issues with patients missing appointments, leading to lost revenue and inefficient scheduling. Manual reminder processes are time-consuming and prone to errors.

## n8n Solution
This n8n workflow is designed to:
1.  **Fetch Appointment Data:** Periodically retrieve upcoming appointment details (e.g., from a dummy Google Sheet or a mock API).
2.  **Format Reminder Message:** Create a personalized reminder message.
3.  **Send Reminders:** Dispatch messages via a dummy SMS/WhatsApp service (e.g., using a mock API or a placeholder for Twilio/WhatsApp nodes).

## Workflow Description
The core of this automation involves:
* **Cron Node:** To schedule the reminder process (e.g., daily at a specific time).
* **HTTP Request Node / Google Sheet Node (Dummy):** To simulate fetching appointment data. For this dummy project, we will assume data is available or mock it.
* **Function Node:** To format the reminder message and handle any conditional logic.
* **HTTP Request Node (for SMS/WhatsApp Mock):** To simulate sending the message to a messaging service. In a real setup, this would be a Twilio, Vonage, or WhatsApp Business API node.

## Setup for Dummy Project
To run this dummy project in your n8n instance:
1.  **Import the workflow:** Download `appointment_reminder_workflow.json` from this folder and import it into your n8n instance.
2.  **Dummy Data:** You can create a simple Google Sheet with columns like `Patient Name`, `Appointment Date`, `Appointment Time`, `Phone Number`. Configure the Google Sheet node in the workflow to read from this sheet.
3.  **Mock API (Optional):** If simulating an SMS/WhatsApp service, you might use a service like [Mocky.io](http://www.mocky.io/) or simply use a Function node to log the intended message.

## Files in This Folder
* `README.md`: This file.
* `appointment_reminder_workflow.json`: The exported n8n workflow for appointment reminders.
* `data/dummy_appointments.csv`: A sample CSV file containing dummy patient appointment data.

## Future Enhancements
* Integration with actual EHR/EMR systems.
* Error handling for failed messages.
* Option for different reminder channels (email, push notifications).
* Patient response handling (e.g., "Confirm," "Reschedule").
