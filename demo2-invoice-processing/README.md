# Demo 2 — AI-Powered Invoice Processing

## Problem
Finance teams receive dozens of invoices by email every month as PDF attachments. 
Someone opens each file, reads the data, and manually copies it into Excel or an 
internal system. This is slow, repetitive, and prone to human error.

## Solution
Automated system that receives emails with PDF invoices, extracts all relevant 
data using Claude AI, logs everything to Google Sheets automatically, and sends 
a confirmation email to the sender.

## How it works
1. Email with PDF invoice arrives in inbox
2. System retrieves the email and extracts the PDF attachment
3. Claude AI reads the PDF and extracts key invoice fields
4. Data is automatically logged to Google Sheets
5. Confirmation email sent to the sender with extracted details

## Data Extracted
- Supplier name
- Invoice number
- Invoice date
- Total amount (with currency)
- VAT amount
- IBAN / payment details

## Stack
- n8n for workflow orchestration
- Claude API (claude-sonnet-4-5) for AI-powered PDF reading and data extraction
- Gmail API for email trigger and confirmation sending
- Google Sheets for structured data logging and audit trail

## Result
A process that took 5 minutes per invoice now runs in seconds, with zero manual 
input, no human errors, and a complete audit trail automatically maintained.

## Screenshots

### Workflow
![Workflow](workflow.png)

### Data logged in Google Sheets
![Data](data.png)
