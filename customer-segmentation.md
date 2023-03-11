# Customer Segmentation by Cohort Analysis and RFM Modelling

##### Capstone Project, Data Science Masters Program (with Simplilearn)

---

<div>
	<img src="https://github.com/ovokpus/Customer-Segmentation/blob/main/img/customer%20segmentation.jpg">
</div>

## Problem Statement

In the retail Industry, it is a critical requirement for businesses to understand the value derived from their customers. RFM is a method used for analyzing customer value.

Customer segmentation is the practice of segregating the customer base into groups of individuals based on some common characteristics such as age, gender, interests, and spending habits.

Our objective here is to perform customer segmentation using RFM analysis. The resulting segments can be ordered from most valuable (highest recency, frequency, and value) to least valuable (lowest recency, frequency, and value).

### Dataset Description

---

This is a transnational data set which contains all the transactions that occurred between 01/12/2010 and 09/12/2011 for a UK-based and registered non-store online retail. The company mainly sells unique and all-occasion gifts.

**Variables Description**

| Variable        | Name                                                  | Info                                                                                                                                       |
| :-------------- | :---------------------------------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------- |
| **InvoiceNo**   | Invoice number                                        | Nominal, a 6-digit integral number uniquely assigned to each transaction. If this code starts with letter 'c', it indicates a cancellation |
| **StockCode**   | Product (item) code                                   | Nominal, a 5-digit integral number uniquely assigned to each distinct product                                                              |
| **Description** | Product (item) name                                   | Nominal                                                                                                                                    |
| **Quantity**    | The quantities of each product (item) per transaction | Numeric                                                                                                                                    |
| **InvoiceDate** | Invice Date and time                                  | Numeric, the day and time when each transaction was generated                                                                              |
| **UnitPrice**   | Unit price                                            | Numeric, Product price per unit in sterling                                                                                                |
| **CustomerID**  | Customer number                                       | Nominal, a 5-digit integral number uniquely assigned to each customer                                                                      |
| **Country**     | Country name                                          | Nominal, the name of the country where each customer resides                                                                               |

---

Below is an Overview of the Dataframe:

![alt text](https://github.com/ovokpus/Customer-Segmentation/blob/main/img/dataframe.jpg)

---

Heatmaps for visualizing Monthly Cohort Metrics

---

### 1. Retention Rates

![alt text](https://github.com/ovokpus/Customer-Segmentation/blob/main/img/monthly_retention_rates.jpg)

---

### 2. Average Quantity

![alt text](https://github.com/ovokpus/Customer-Segmentation/blob/main/img/avg_quantity_monthly.jpg)

---

### 3. Average Spend

![alt text](https://github.com/ovokpus/Customer-Segmentation/blob/main/img/avg_spend_monthly.jpg)

---

### Finally, we have a Dashboard to show the various RFM metrics:

![alt text](https://github.com/ovokpus/my-bi-gallery/blob/main/images/rfm-dashboard.png)

---
