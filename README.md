# FreightFlow AI: Dispatch & Billing Anomaly Detector

Building AI course project by Farhan Jama Hussein.

## Summary
An AI-powered assistant for small-to-midsize trucking and logistics operations that automates load-to-driver matching, predicts route fuel and carbon costs, and flags billing or invoicing discrepancies before payment processing.

## Background
Trucking dispatchers and billing specialists spend hours manually cross-checking rate confirmations, bills of lading (BOLs), detention charges, and fuel surcharges. Human error in rate entry or suboptimal route assignments leads to delayed invoices, revenue leakage, and wasted fuel.

## How is it used?
* **Smart Dispatch:** Dispatchers input available loads and driver locations; the system recommends optimal multi-stop routes minimizing empty miles and CO2 emissions.
* **Automated Billing Audit:** Before an invoice is finalized, the AI scans extracted text from rate confirmations and BOLs, flagging unusual variances in linehaul rates, accessorial fees, or mileage.

## Data sources and AI methods
* **Data sources:** Historical dispatch logs, rate confirmation PDFs, freight distance matrices, and invoice records.
* **AI methods:**
  * **Route Optimization / Simulated Annealing:** Inspired by Chapter 1 (*Optimization & Hill Climbing*), to solve multi-stop routing and minimize empty deadhead miles.
  * **Linear Regression:** Inspired by Chapter 3 (*Linear Regression*), to predict expected freight rates and fuel costs based on distance, weight, and equipment type.
  * **Naive Bayes / TF-IDF Text Classification:** Inspired by Chapters 2 & 3, to categorize incoming broker emails and flag high-risk or anomalous billing documents.

## Challenges
* **Messy Document Formats:** Broker rate confirmations vary widely in layout, requiring reliable OCR and text extraction before classification.
* **Edge Cases in Accessorials:** Unplanned delays (detention or layovers) require human verification so the model does not falsely flag legitimate extra charges as errors.

## What next?
Build a working Python prototype for the rate anomaly detector and integrate a lightweight web dashboard for dispatchers to review flagged invoices.

## Acknowledgments
* The [Elements of AI](https://www.elementsofai.com/) and [Building AI](https://buildingai.elementsofai.com/) team at the University of Helsinki and MinnaLearn.
