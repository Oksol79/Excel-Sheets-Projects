# Data Analyst Portfolio 
This portfolio showcases the hands-on projects I completed to build my skills in Excel, Google Sheets, SQL, Python, Matplotlib, Seaborn, and others. In my projects, I demonstrate my ability to:
 - clean, process, and analyze data;
 - create dynamic reports and dashboards;
- interpret results to make informed decisions.

Each project showcases my analytical approach and drive to transform data into actionable business insights.
## Table of Contents
- [Projects](#projects)
  - [Project 1: Sales Dynamics & ABC Analysis](#project-1-sales-dynamics--abc-analysis)
  - [Project 2: FCA based Ontology for Intelligent Diagnostics](#project-2-fca-based-ontology-for-intelligent-diagnostics)
- [Skills Demonstrated](#skills-demonstrated)
- [Tools Used](#tools-used)
- [Key Features Used](#key-features-used)
- [Contact](#contact)


## Projects
### Project 1: Sales Dynamics & ABC Analysis
[View Project]()  

In this project, I analyzed and visualized sales dynamics by category, product, and country, and conducted ABC analysis using the Pareto principle. For my work, I used three tables from a dataset imported into Google Sheets:
 - Events - information about orders and sales.
 - Products - product category. 
 - Countries - geographic data.

The data was imported into Google Sheets, where a full analytics cycle was performed - from data quality checks to creating an interactive dashboard.  
#### Project steps:  
**Step 1. Data preparation and cleaning**  
Checked the quality and integrity of data in all tables: errors, anomalies, and incorrect values ​​were detected. Processing of missing data was performed. New calculated columns were added to the Events table: Total Revenue, Total Cost, Total Profit, Profit Margin (%), and data from other tables was added.  

**Step 2. The company's key business metrics were selected**  
The company's key performance metrics were calculated: Total number of orders, Total revenue and profit, Number of countries covered, Average profit per order.

**Step 3. Sales Analytics**   
Sales were analyzed by product category, geography, and sales channels.  
By product category: The most popular categories were identified, The revenue, expenses, and profit for each category were analyzed.  
By geography: Sales by country, region, and subregion, The markets with the highest profitability indicators were identified.  
By sales channel: The effectiveness of online and offline channels was compared.  

**Step 4. Order fulfillment time analysis**  
The interval between order and shipment was analyzed by: product categories, countries, regions. It was investigated whether delivery speed affects profitability.

**Step 5. Analysis of sales dynamics**
The dynamics of sales by year, month, and day of the week were analyzed. The day of the week was determined using the WEEKDAY() function. The main trends and seasonal patterns were determined.  

**Step 6. Visualization of results**
A dashboard was created in Google Sheets with interactive graphs and charts. Key indicators were visualized: sales dynamics over time, profit by category and by country, and the online/offline sales ratio.

**Step 7. ABC analysis**
ABC analysis of products was conducted by sales volume, revenue, and profit (for the last year). Products were divided into categories A, B, and C according to the Pareto principle (80/20).

**8. Key findings**
The most profitable product categories and countries were identified. The relationship between delivery speed and profitability was found.
The periods with the highest sales volumes were determined. Analytical recommendations were formed for optimizing the assortment and logistics.

<img width="1898" height="867" alt="image" src="https://github.com/user-attachments/assets/e596379f-6445-4de7-a047-8abe077416bc" />

### Project 2: FCA based Ontology for Intelligent Diagnostics
[View Project]()  
[Link to article](https://ieeexplore.ieee.org/document/6662995)

This project presents an ontology for the domain "Intelligent Diagnostics of Computer Systems", developed based on expert knowledge and evaluations.
The ontology integrates concepts from two interconnected fields:
- Intelligent diagnostics of computer systems.
- Artificial intelligence (AI).

**Methodology**  
To construct the ontology and organize the domain concepts into a taxonomy, the project applies Formal Concept Analysis (FCA).
To do this, the project:
 - A set of attributes is selected, considering the relationships defined for each concept.
 - The attribute set is verified for normalization to ensure logical consistency and completeness.

The base taxonomy is enhanced with non-taxonomic semantic relations to represent richer conceptual connections and enable more diverse queries.
An ontology is a special type of knowledge base that can be read, interpreted, separated from the developer, and/or physically shared by users.
To build an ontology of the subject area "Intellectual diagnostics of computer means" based on expert representations and assessments, the following were developed:
 - A taxonomy of classes of concepts of the subject area.
 - A structure of concepts and relations of this subject area was formed.
 - A set of axioms was formed to limit the interpretation of concepts of the subject area.

**Method for forming a taxonomy of classes**  
One of the basic components of the ontology is a taxonomy of concepts, which involves classifying concepts in the subject area and constructing a hierarchical structure of classes.
A taxonomy of concepts was formed for each of the above subject areas separately.
To develop a taxonomy:
 - A complete list of terms (concepts) of the subject area was created, regardless of their properties and relations.
 - Сlasses and types of relations were defined, and a hierarchy of classes was developed (concepts were specified according to the class-subclass principle).
 - The properties of concepts were defined.  

Two levels of diagnostic information were used, which are the basis for highlighting basic concepts and their properties for the specified subject areas:
1) The level of explicit diagnostic information is diagnostic information presented in the form of messages, letters, directories, patents, algorithms, etc.
2) The level of hidden (personal) diagnostic information is the individual experience of diagnosticians, presented in the form of verbal descriptions.  

As the source material for constructing the ontology, we will use tables with diagnostic information of the type "object - property": (D,R), D ≠ ∅, R ≠ ∅, where D - a set of objects, and R - a set of properties of these objects.
The result of constructing the table is the establishment of binary relations between objects and properties. The rows of the table correspond to objects of the subject area, and the columns reflect the set of properties of these objects (Table 1).  
Table 1 - Example of a tabular representation of diagnostic information about objects and their properties

<img width="532" height="278" alt="image" src="https://github.com/user-attachments/assets/c569ff69-94e3-46ad-b764-6eff5b9b5724" />

To build the class structure, the following tasks were solved:  
- formation of initial data on the subject area.
- analysis of relationships between objects and properties.  

To solve the first task, the knowledge of diagnostic experts was used, on the basis of which the tables were filled in.  
To solve the second task, a method of automated formation of a taxonomy of concept classes was developed.  
The basic information for distinguishing classes is the statement of the fact of the presence of certain properties in individual objects or groups of objects.  
The method of forming a taxonomy of classes in a subject area is as follows. First, we form an abstract class structure:
1) Remove all "0" columns from the table, since this means the absence of such a property in objects of the subject area. The reason may be an expert error, the inability to detect a property, for example, the absence of devices that can detect a property, etc.
2) If there is a "0" row - enter a new column with an "abstract property" and assign it the value "1" for this row (there is no diagnostic information characterizing the object yet).
3) The number of obtained property columns determines the number of hierarchy levels in the class taxonomy.
4) We form a superclass from objects for which the values ​​of all columns are "1".
5) While there are columns, we form subclasses for this class from objects that have one more zero column. The number of subclasses of the class is equal to the number of non-zero columns.  

In the obtained abstract structure, we record real (those for which objects and properties are defined) and abstract classes (for which there is not enough diagnostic information yet).  
The procedure for forming the class structure is iterative and allows us to detect incompleteness of the description of the subject area. If the number of abstract classes is relatively large (in percentage terms), then either the subject area has many exceptions, or the set of object properties is defined inefficiently.  

<img width="1909" height="891" alt="image" src="https://github.com/user-attachments/assets/88bd6c3a-7f93-4e10-8ff6-0a9e6e620950" />

As a result of processing the table with diagnostic information based on the proposed method, the following are performed:
 - Classification of objects of the subject area "Intelligent diagnostics of computer means".
 - Aggregation of objects (by combining them into classes).
 - Association of objects (based on the distance between classes, which is determined by the number of different properties for two classes).

The developed basic taxonomy of classes of objects of the subject area "Intelligent diagnostics of computer means" can be supplemented when new diagnostic information appears.
Based on the proposed method, an algorithm for automatic generation of class taxonomy has been developed.






## Skills Demonstrated





## Tools Used





## Key Features Used



## Contact
Feel free to connect with me via LinkedIn:  
https://www.linkedin.com/in/oksana-olar-993709162/
