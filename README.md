# n8n-Orchestrated LLM Receipt-to-Sheets Automation

An end-to-end automation workflow built with **n8n** that processes receipt images sent via **Telegram**, extracts structured expense data using an **LLM with schema-based parsing**, and stores the results in **Google Sheets**. The project demonstrates real-world workflow orchestration, document understanding, and automated data pipelines.

---

## Problem

Manual expense tracking from receipts is time-consuming, error-prone, and inconsistent, especially when receipts arrive as unstructured images or PDFs.

---

## Solution

This project implements an automated pipeline that ingests receipt images via Telegram, retrieves and processes the files, extracts structured expense information using an LLM, and appends the cleaned data into Google Sheets. A confirmation message is sent back to the user, completing the automation loop.

---

## Workflow Overview

1. **Telegram Trigger** – Listens for incoming messages containing receipt images  
2. **File Retrieval** – Downloads the receipt file from Telegram  
3. **LLM-Based Extraction** – Converts receipt content into structured JSON using a predefined schema  
4. **Data Preparation** – Normalizes extracted fields for spreadsheet storage  
5. **Google Sheets Insertion** – Appends structured expense data  
6. **User Confirmation** – Sends a confirmation message back via Telegram  

---

## Architecture
<img width="797" height="363" alt="Screenshot 2026-02-09 at 21 58 21" src="https://github.com/user-attachments/assets/24fbbc2a-273c-4edc-804e-4771596ef753" />
Telegram → n8n → LLM (Structured Extraction) → Google Sheets → Telegram


---

## Tech Stack

- **n8n** – Workflow orchestration  
- **OpenAI LLM** – Structured data extraction  
- **Telegram Bot API** – Receipt ingestion and user feedback  
- **Google Sheets API** – Expense data storage  

---

## Setup Instructions

1. Clone the repository  
2. Import the workflow JSON into your n8n instance  
3. Configure credentials for:
   - Telegram Bot
   - OpenAI
   - Google Sheets
4. Update environment variables as needed  
5. Activate the workflow  

---
