# PowerBI-Fauget_Downtime_Defect_Analysis
## I. OVERVIEW
The manufacturing plants operated by the Fauget Group encountered various challenges in 2022, resulting in a notable decline in supply performance. These issues, primarily stemming from downtime at the large factories, had significant repercussions, including business interruptions and production delays. Customers expressed dissatisfaction due to irregular delivery progress and concerns about product quality. Moreover, the company faced financial challenges as a result of overspending in the supply chain, increased labor and material costs, and the potential loss of customers.

In response to these challenges, it is imperative for the Fauget Group to conduct a comprehensive review of supply activities and factory productivity to identify the root causes of these issues and implement corrective measures to enhance operational efficiency and customer satisfaction.

## II. DATASETS
![image](https://github.com/Tann1901/PowerBI-Fauget_Downtime_Defect_Analysis/assets/108020327/18d6666a-4a64-49ac-a591-af8cdfdd20e6)
DATASET incude:
8 dimension tables:
-Date
-Material
-Vendor
-Plant
-Cost
-Defect
-Defect_rating
-Category

 1 Fact Table:
-Metrics (> 1000 rows)
## III. DATA WRANGLING
UPDATE & COMBINING
EXCEL: COMBINE DATASET INTO COST
Import more information about loss prices to get a realistic and accurate view of the data
![image](https://github.com/Tann1901/PowerBI-Fauget_Downtime_Defect_Analysis/assets/108020327/9dc01d1b-b19f-4b11-b8b7-9080ed035380)

CLEANING
EXCEL: BRIEF VISUAL DATA CHECK
Check and eliminate duplicate data lines (duplicates)
Identify and remove NULL data lines.
Identify unnecessary columns and remove them.
Adjust the column names to be clear and easy to name when coding
Use Filter to check spelling and edit with `Find & Replace`.
Filter time frame in 2022

SQL: CHECK UNIFORMITY
Join tables to determine the accuracy and reasonableness of metrics tables before putting them into use
![image](https://github.com/Tann1901/PowerBI-Fauget_Downtime_Defect_Analysis/assets/108020327/5f21caf4-ed39-4665-8e52-ba74c7dd55e7)
![image](https://github.com/Tann1901/PowerBI-Fauget_Downtime_Defect_Analysis/assets/108020327/bcc52371-d806-4760-be5f-141814a16aea)

CONFIRM DATA TYPE 
POWER BI: VISUALIZE DATA
Model View
![image](https://github.com/Tann1901/PowerBI-Fauget_Downtime_Defect_Analysis/assets/108020327/d516d9ca-481c-417a-acd1-0366749a22a3)

Use Merge Data for Merging tables
![image](https://github.com/Tann1901/PowerBI-Fauget_Downtime_Defect_Analysis/assets/108020327/4ff4384b-7229-43cd-8f31-aa7f927aeebd)

Transform data for map
![image](https://github.com/Tann1901/PowerBI-Fauget_Downtime_Defect_Analysis/assets/108020327/292824c1-1da3-499d-8bb0-1ce3ea01a907)

## IV. DATA VISUALIZATION, INSIGHTS AND SUGGESTIONS
![image](https://github.com/Tann1901/PowerBI-Fauget_Downtime_Defect_Analysis/assets/108020327/da85e3c8-b235-42f8-8e03-f3f8b0bc2a6f)
ANALYZE DEFECT

The most significant proportion of product defects, comprising 38.73% of the total, results in errors that impact the group's revenue, leading to damage and compensation issues in customer contracts. Following closely are product errors that customers refuse to return, and the lowest proportion, at 26.87%, relates to low-impact errors. These low-impact errors may be accepted by customers but still cause damage within the production facility, resulting in increased repair time, labor costs, and strain on interdepartmental relationships.

Among the defective materials, crates are responsible for the most significant losses, with approximately 600,000 defective products. In contrast, electrolytes are among the top five materials causing numerous product errors, but their impact on the group's revenue is minimal. Notably, film is responsible for the fewest defective products, with fewer than 100,000 affected items.

When categorizing product defects by industry, it becomes evident that the top four industries with the most defective products are goods & services, logistics, packaging, and electronics, respectively.

SOLUTION SUGGESTED

To address these issues, the Group's approach involves prioritizing the identification of suppliers capable of meeting the required material quality standards for products prone to defects, such as tanks, engines, and molds. This approach aims to enhance overall revenue.

Furthermore, the factory must focus on resolving errors that lead to substantial losses, as they are a primary contributor to the current overspending problem. Investigating the root causes of these errors, whether they stem from materials, suppliers, or production lines, is essential. These errors have a direct impact on critical product categories, particularly in packaging and logistics. Failure to rectify them could result in the loss of significant customers in these industries.

On the supplier side, suppliers should take particular care to ensure the quality of the materials they provide before delivering them to customers like the Fauget Group.

![image](https://github.com/Tann1901/PowerBI-Fauget_Downtime_Defect_Analysis/assets/108020327/e066c76d-b5bb-40b4-9b7a-98d03f1eb20e)
ANALYZE DOWNTIME

Machine downtime refers to the hours during which production lines come to a halt due to errors in the manufacturing process, as mentioned in the previous slide. The downtime associated with different materials used shows that the use of materials such as cardboard boxes, thin wood boxes, hard drives, or motors tends to result in more errors and the longest periods of machine downtime. Additionally, when producing products for industries supplying raw materials, services, and mechanics, the downtime is also prominently high, as indicated in the analytical chart. This highlights the interplay between industries and the materials used in their respective product lines.

Overall, machine downtime in 2022 exhibited an upward trend, increasing by 18.64%, while the total number of defective products showed a decreasing trend by 9.22%. It's worth noting that the highest number of defective products occurred in June, while machine downtime peaked in October during the year 2022.

SOLUTION SUGGESTED

=>The Group should focus on rectifying errors caused by materials that lead to the longest machine downtime and should closely examine the production processes at stages where these materials are used (cardboard boxes, thin wood boxes, hard drives, or motors). Continuously monitor and update results after rectifying the material-related issues and collaborate with the sales revenue department in critical industries (raw materials supply, services, mechanics).

=>Record the high peak months of machine downtime and work with relevant departments to identify the causes (both objective and subjective factors, such as increased orders in certain months, machinery malfunctions, labor errors, low material supply, disease outbreaks, etc.).

![image](https://github.com/Tann1901/PowerBI-Fauget_Downtime_Defect_Analysis/assets/108020327/6533cfab-7d68-459b-ab6f-24d20f7edb22)
ANALYZE DOWNTIME LEADING DEFECT COST

It is evident that the extent of damage is most significantly influenced by customer-rejected errors, accounting for $26.53 million, followed by errors affecting final revenue, with errors having no impact coming in last.

As per the previous analyses, it is noteworthy that the use of crates as a material results in the highest number of defective products, and the use of printed materials leads to the most substantial damage. These findings align with the sectors of service production, packaging, and logistics, where special attention is required.

SOLUTION SUGGESTED

1. Propose an inspection plan and a return policy for deliveries to customers, considering errors caused by manufacturers or transportation providers, objective errors, and the timing and method of returns. This approach aims to reduce the number of rejected products.
2. Negotiate with material suppliers to reduce purchase costs, establish standards for each type of material, with particular focus on crates and printed materials.
3. Provide training and ensure strict oversight of the Quality Control (QC) department, tightly monitoring the product output process to minimize losses resulting from rejected deliveries or compensation for orders.

![image](https://github.com/Tann1901/PowerBI-Fauget_Downtime_Defect_Analysis/assets/108020327/8b42301e-b342-4d62-8c0b-19c9a18fd380)
ANALYZE PLANT

From the list of factories within the conglomerate, let's identify the top 5 factories that produce a high number of products leading to rejected deliveries and the top 5 factories that produce products with the most severe defects.

From the bar chart, we can observe that the Kalamazoo factory has the highest total machine downtime, nearly 5000 hours, which is over 50% more than the Elgin factory, which has the lowest machine downtime. This implies that these two factories correspond to the highest and lowest levels of damage, respectively.

SOLUTION SUGGESTED

The conglomerate should conduct inspections at the factories with high machine downtime regarding materials, machinery condition, labor, and management. It is recommended to consider replacing machinery after comparing the cost of purchasing new machines with the compensation cost for defective products.

![image](https://github.com/Tann1901/PowerBI-Fauget_Downtime_Defect_Analysis/assets/108020327/23729b77-d018-426b-be78-80cf94aac320)

ANALYZE VENDOR

When examining the vendors ranking tables, it's evident that suppliers like Rolamice, Dan-High, and Trueplus consistently rank in the top 5 suppliers causing damage, having high machine downtime, and producing the highest number of defective products.

In particular, when observing the two line charts, Rolamice stands out with the highest total machine downtime and the most significant level of damage compared to the other suppliers.

SOLUTION SUGGESTED

The conglomerate should consider reevaluating their collaboration with these suppliers that are responsible for errors affecting revenue and rejections to reduce machine downtime and enhance the overall supply performance of these suppliers. Additionally, negotiations can be undertaken to potentially renegotiate material procurement prices from these suppliers while also revising supply contracts to tightly control the quality of incoming materials.

## V. CONCLUSIONS
**External Suggestions:**

1. Implement a Supplier Scoring Process: Develop a supplier performance scoring system to assess and monitor the reliability, quality, and delivery capabilities of your suppliers. This will help in making informed decisions about supplier relationships and identifying areas for improvement.

2. Switch Providers: Consider evaluating alternative suppliers for critical materials or components to diversify your supply chain. This can help mitigate risks associated with relying on a single source and provide better negotiation leverage.

3. Re-negotiate Prices of Imported Materials and Market Prices: Given the rising costs of materials, explore opportunities to re-negotiate pricing agreements with your suppliers. Additionally, regularly monitor market prices and adapt your purchasing strategies accordingly to optimize costs.

4. Review Agreements with Suppliers (Material Quality, Return Methods): Revisit existing agreements with suppliers, especially those related to material quality and return procedures. Ensure that these agreements align with your quality standards and that there are clear processes for returning subpar materials.

5. Directing Quality Assurance and Quality Control: Strengthen your in-house quality assurance and quality control processes. This involves conducting regular inspections and quality checks to maintain product consistency and meet customer expectations.

**Internal Suggestions:**

1. Integrate with Plant/Corporate Operations: Ensure seamless integration of your supply chain and manufacturing operations with the overall activities of the plant or corporation. This alignment can improve communication and coordination.

2. Examine System Upgrades for Common Errors: Review and upgrade your systems, especially those prone to common errors. Implementing technological improvements can enhance efficiency and reduce downtime.

3. Negotiate Prices and Terms with Customers: Initiate negotiations with your customers to reevaluate pricing and contractual terms. This can help create more mutually beneficial agreements and improve customer relations.
