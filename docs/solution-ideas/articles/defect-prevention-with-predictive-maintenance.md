---
title: Defect prevention with predictive maintenance
titleSuffix: Azure Solution Ideas
author: adamboeglin
ms.date: 12/16/2019
description: Learn how to use Azure Machine Learning to predict failures before they happen with real-time assembly line data.
ms.custom: acom-architecture, manufacturing control, quality control process, anomaly-detection, manufacturing quality control, 'https://azure.microsoft.com/solutions/architecture/defect-prevention-with-predictive-maintenance/'
ms.service: architecture-center
ms.category:
  - ai-machine-learning
  - analytics
ms.subservice: solution-idea
social_image_url: /azure/architecture/solution-ideas/articles/media/defect-prevention-with-predictive-maintenance.png
---

# Defect prevention with predictive maintenance

[!INCLUDE [header_file](../../../includes/sol-idea-header.md)]

Learn how to use Azure Machine Learning to predict failures before they happen with real-time assembly line data.

This solution is built on the Azure managed services: [Azure Stream Analytics](https://azure.microsoft.com/services/stream-analytics), [Event Hubs](https://azure.microsoft.com/services/event-hubs), [Machine Learning Studio](https://azure.microsoft.com/services/machine-learning-studio), [Azure Synapse Analytics](https://azure.microsoft.com/services/synapse-analytics) and [Power BI](https://powerbi.microsoft.com). These services run in a high-availability environment, patched and supported, allowing you to focus on your solution instead of the environment they run in.

## Architecture

![Architecture Diagram](../media/defect-prevention-with-predictive-maintenance.png)
*Download an [SVG](../media/defect-prevention-with-predictive-maintenance.svg) of this architecture.*

## Components

* [Azure Stream Analytics](https://azure.microsoft.com/services/stream-analytics): Stream Analytics provides near real-time analytics on the input stream from the Azure Event Hub. Input data is filtered and passed to a Machine Learning endpoint, finally sending the results to the Power BI dashboard.
* [Event Hubs](https://azure.microsoft.com/services/event-hubs) ingests raw assembly-line data and passes it on to Stream Analytics.
* [Machine Learning Studio](https://azure.microsoft.com/services/machine-learning-studio): Machine Learning predicts potential failures based on real-time assembly-line data from Stream Analytics.
* [Azure Synapse Analytics](https://azure.microsoft.com/services/synapse-analytics): Synapse Analytics stores assembly-line data along with failure predictions.
* [Power BI](https://powerbi.microsoft.com) visualizes real-time assembly-line data from Stream Analytics and the predicted failures and alerts from Data Warehouse.

## Next steps

* [Learn more about Stream Analytics](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-introduction)
* [Learn more about Event Hubs](https://docs.microsoft.com/azure/event-hubs/event-hubs-what-is-event-hubs)
* [Learn more about Machine Learning](/azure/machine-learning/overview-what-is-azure-ml)
* [Learn more about Synapse Analytics](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-overview-what-is)
* [Learn more about Power BI](https://powerbi.microsoft.com/documentation/powerbi-landing-page)
