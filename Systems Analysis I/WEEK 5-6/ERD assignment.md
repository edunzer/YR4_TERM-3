## ERD ASSIGNMENT

Introduction
	In this assignment you will create an Entity Relationship Diagram that captures the information needed in the APC Case. As before, set up the context for the assignment.
    •	Explain the purpose of this assignment, and how it relates to what we are doing in class. The assumption here is that you have taken database classes and are familiar with the structure of ERDs. If that is not true, then you should contact me for some one-on-one time to go over the elements of an ERD.
    •	Setup up the context of the paper for the APC reader. Why do they care about this?
    •	Provide a brief overview of each section below

  APC needs to expand and capitalize on their current standing in the publishing house market. The goal of APC to increase their business growth by 85% over the next 3 years. This will be achieved by creating better tracking then the current system has to offer, create better relationships with authors, creating a better outreach process to help their appearance to outside authors, and to adjust there “ideal market image” by what is trending.

  The new system not only has to upgrade hardware components of their current system but also the functionality of it. In order to streamline their new business processes, they need to shift from a paper-based system to digital in order to keep accurate and better track of their projects. This will help with efficiency, but also information loss which they detailed as a huge problem in their current system. Since all projects will be digital, they can be further organized and categorized by genre and trend to make decisions for the collective easier.

  The following information contains a detailed explanation of all high-level business processes and how they will function in APC’s workflow. Also, there is a use-case diagram that shows the connections between each employee and there high-level business process that they will be using in order to complete there day to day tasks.


Topic Analysis

Part 1: Identify the entities for whom you need to store data
  •	Provide a setup/introduction to explain to APC what the section does and define any new terms.
  •	Identify those entities (person, place or thing) about which you need to collect information. The Dataflow Diagram highlighted the process and the data that flows between them. The ERD highlights those objects about which the data is collected.
  •	Demonstrate that your understand the relationships between the entities and the functional requirements You have figured out the business rules of APC through your understanding of the requirements and the processes that are generated from them.
  •	Now think about the elements within the project that are supported by the data stores you found in the Data Flow diagram. For example, one of the use cases surely supported the journey of the manuscripts from author to APC and then on to the publishing process. One obvious entity then would be the manuscript. Another might be the contract, etc.
  •	Provide a summary for the section to help the APC make sense of what you have discovered here

  In this section APC's new business entities will be laid out for readers to view. Each entity is a certain aspect of APC's new workflow system which will be put in place to improve productivity. All these different entities have self explanatory names but will be further defined in the following information:

  Manuscripts

  Authors

  Ledger Cards

  Accounts

  Inventory

  Orders

  Contracts

  Illustrations/Artwork

  Printers

  Sponsorship

  Employee's



Part 2: Identify the attributes of interest for each entity
  •	Provide a setup/introduction to this section to help the reader understand the importance of getting the right attributes identified through the requirements
  •	Given that you have identified the entities (aka as tables in the database context), identify the attributes of those attributes that you need to store to service the use cases you have identified. Resist the urge to add anything you think might be useful to them in the future. For now just add those attributes that are required to service the requirements.  This is an iterative process in the real world, so you may discover additional attributes later that you missed on the first pass. Just explain why you choose these attributes and relate them to the requirements (RID) they are designed to service. These attributes, plus a primary key, become the attributes you use to populate each table within the ERD.
  •	Create a table to show the data type, length and any constraints for each of the attributes
  •	Provide a summary for the APC reader to make sure they understand the relationship between the attributes and the functional requirements

  In this section APC's attributes for each given entity will be explained and outlined. These attributes will be the variables and content that will fill the entity. Each variable will have a different type of value. In this given case there are only two use values int, which stands for integer, and varchar, which stands for character data. These different variables will be assigned to the many entities in the following information:

  Manuscripts
    Title - varchar
    Author - varchar
    ID - int
    Status - varchar
    ISBN - varchar
    Link - varchar

  Authors
    First name - varchar
    Last name - varchar
    Phone - int
    Email - varchar
    Ledger link - varchar

  Ledger Cards
    Name - varchar
    Type - varchar
    ID - int
    Value - int
    Spreadsheet link - varchar

  Accounts
    Name - varchar
    Type - varchar
    ID - int
    Value - int
    Spreadsheet link - varchar

  Inventory
    Title - varchar
    Amount - int
    Requests - int
    Status - varchar

  Orders
    Title - varchar
    ISBN - varchar
    Amount - int
    Info - varchar
    Status - varchar

  Contracts
    Title - varchar
    Contract Link - varchar

  Illustrations/Artwork
    Title - varchar
    Manuscripts - varchar
    Status - varchar
    Link - varchar

  Printers
    Name - varchar
    Avg Price - int
    Num Previous Jobs - int
    Info - varchar

  Sponsorship
    Name - varchar
    Avg Price - int
    Num Previous Jobs - int
    Info - varchar

  Employee's
    First name - varchar
    Last name - varchar
    Email - varchar
    Phone - int
    ID - int
    Type - varchar
    Access level - int

Part 3: Establish the relationships between the entities
  •	Provide a setup/introduction to this section to help the reader understand the importance of identifying the relationships between entities  
  •	Using Visual Paradigm, create tables and include the primary key for the table and any foreign keys needed to relate to other tables. Remember, if you relate two tables, then one has the primary and the other needs to have the same key used as a foreign key.
  •	Tell the reader about the relationships and identify their cardinality. Use Visual Paradigm to create your ERD. Show the relationships and the cardinality between tables. Remember that just showing the ERD is not sufficient. Be sure to make the connection between the functional requirements list and your final ERD.
  •	You need to provide a clear explanation of what you did and why you did it. please include a figure # and descriptive title for each graphic. If your graphic is too large to read when you embed it in your doc, then screenshot sections of it to flow with your explanations.
  •	Provide a Summary for the APC reader to help them understand the significance of the ERD for their system design.

  In this section APC's new entities will show the given relationships that they have with other entities. These relationships are how they will communicate and exchange data. In these relationships there are several different ways to communicate. First we have One, then Many, then One(and only one), then zero or one, then one or many, and finally zero or many. These relationships are there to show how one entity will perceive another. For example an entity of "orders" would have a one to one relationship with an entity called "customers" because there can only be one customer per order and there has to be a customer for an order. The entity relationships for APC's entities will be shown in the following information:

  Manuscripts Authors
  Manuscripts Sponsorship
  Manuscripts Contracts
  Manuscripts Printers
  Manuscripts Illustrations/Artwork
  Manuscripts Inventory

  Authors Manuscripts
  Authors Contracts

  Ledger-Cards Accounts
  Ledger-Cards Contracts
  Ledger-Cards

  Accounts Ledger-Cards

  Inventory Orders
  Inventory Manuscripts

  Orders Inventory

  Contracts Authors
  Contracts Ledger-Cards
  Contracts Manuscripts

  Illustrations/Artwork Manuscripts

  Printers Manuscripts

  Sponsorship Manuscripts

  Employee's Ledger-Cards

Conclusion
  •	Provide a clear summary of what you learned in the exercise.
  •	Demonstrate your understanding of the purpose and uses of an Entity Relationship Diagram and identify when you would use this tool. Identify how this tool would be used with the stakeholders of the project

If you use references, put them on a separate reference page with APA formatted references
