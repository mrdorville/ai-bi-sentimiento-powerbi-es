# AI + BI: Sentiment Analysis in Power BI with Azure AI Language

This repository demonstrates how to integrate **Azure AI Language (Text Analytics)** with **Power BI** to perform sentiment analysis on Spanish text data.  
It includes an anonymized dataset, M scripts, and best practices to help you build an AI-enhanced Business Intelligence dashboard without exposing sensitive credentials.

## Overview

The goal of this demo is to show how **Artificial Intelligence (AI)** and **Business Intelligence (BI)** can work together to transform user feedback and comments into strategic insights.  
Using **Azure AI’s Text Analytics API**, Power BI connects directly to the service, processes natural language, and visualizes sentiment distributions, trends, and key indicators in real time.

## Architecture

**Data Flow**

CSV Dataset (Spanish reviews) → Power BI Desktop → Power Query (M Function: fxSentiment) → Azure AI Language – Text Analytics API → Sentiment Scores & Confidence → DAX Measures & Visuals

## Repository Structure

ai-bi-sentiment-powerbi-es/
│
├─ data/
│ └─ resenas_es_600_ascii.csv
│
├─ scripts/
│ └─ fxSentiment_anonimo.txt
│
├─ docs/
│ └─ presentation_barcamp2025.pdf
│
├─ .gitignore
└─ README.md

## Requirements

- Power BI Desktop (latest version)  
- Azure Subscription with **AI Language (Text Analytics)** resource  
- API Endpoint and Key (configured as parameters in Power BI)  
- Basic understanding of **Power Query (M)** and **DAX**

## Quick Start

1: Download or clone this repository:
     command: git clone https://github.com/rafaeldorville/ai-bi-sentimiento-powerbi-es.git
  2: Open Power BI Desktop.
  3: Load the CSV file from data/resenas_es_600_ascii.csv.
  4:
    Create two parameters in Power BI:
      - EndpointTextAnalytics → your Azure Text Analytics endpoint
      - ApiKeyTextAnalytics → your subscription key
  5: Import the M script from /scripts/fxSentiment_anonimo.txt into Power Query.
  6: Invoke the function fxSentiment over your text column to obtain sentiment and confidence scores.
  7: Visualize results using DAX measures and Power BI visuals.

## Example Insights

- Overall sentiment distribution  
- Sentiment by product, service, or region  
- Confidence average by sentiment  
- Positive/negative trend analysis  
- Real-time visualization and storytelling  

## Best Practices

- Never hardcode API keys; always use parameters.  
- Keep datasets small when using free-tier Azure resources.  
- Batch large datasets to avoid rate limits (HTTP 429).  
- Exclude `.pbix` and `.pbit` files using `.gitignore`.  
- Use Power Query transformations for data cleaning and preprocessing.  

## Learn More

- [Azure AI Language Service Documentation](https://learn.microsoft.com/en-us/azure/ai-services/language-service/)  
- [Power BI Power Query M Reference](https://learn.microsoft.com/en-us/powerquery-m/)  
- [Text Analytics REST API](https://learn.microsoft.com/en-us/azure/ai-services/language-service/sentiment-opinion-mining/overview)  

## Resources

- Dataset: `/data/resenas_es_500_ascii.csv`  
- Power Query Script: `/scripts/fxSentiment_anonimo.txt`  
- Presentation: `/docs/presentation_barcamp2025.pdf`  

## Author

**Rafael Miguel Dorville Collado**  
Cloud & Data Solutions Engineer | AI & BI Instructor  
[LinkedIn](https://www.linkedin.com/in/rafaeldorville) • [GitHub](https://github.com/rafaeldorville)  

## License

This project is licensed under the **MIT License** – see the LICENSE file for details.=
