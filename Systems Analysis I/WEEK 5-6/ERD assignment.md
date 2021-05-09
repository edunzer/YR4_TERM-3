## ERD ASSIGNMENT

Introduction
	In this assignment you will create an Entity Relationship Diagram that captures the information needed in the APC Case. As before, set up the context for the assignment.
    •	Explain the purpose of this assignment, and how it relates to what we are doing in class. The assumption here is that you have taken database classes and are familiar with the structure of ERDs. If that is not true, then you should contact me for some one-on-one time to go over the elements of an ERD.
    •	Setup up the context of the paper for the APC reader. Why do they care about this?
    •	Provide a brief overview of each section below

  The purpose of this assignment is to create a document for the APC employees to view and see how different data store entities work, relate, and function in there new system. This document will also work to outline the different types of data that will go into each one of the entities and how that data will be connected to other entities.

  Throughout the document there will be detailed sections about what the different entities are, what attributes and data types they have, and how and why they connect the way they connect. All these sections are labeled for the reader and have been explained to make sure the reader knows what is happening.

Topic Analysis

Part 1: Identify the entities for whom you need to store data

  In this section APC's new business entities will be laid out for readers to view. Each entity is a certain aspect of APC's new workflow system which will be put in place to improve productivity. All these different entities have self explanatory names but will be further defined in the following information:

    Manuscripts - This is a data store for all the manuscripts that have come into APC. It doesn't matter what stage they are at or if they are already printed; this is where they are stored. This means that all access to manuscripts is through this entity.

    Authors - This is a data store for all the authors that have come to APC.

    Ledger Cards - This is a data store for all the ledger cards that APC has created to keep track of accounts. Ledger cards are seen as the filling system for APC and they display the main information for different accounts that relate to authors, printers, sponsorship, etc. and will have a link to the spreadsheet that has the actual finance accounting. Think of it as the contact list for all financial dealings.

    Accounts - This is a data store for all the financial accounts that APC has. This could range from business operation finances to deals with sponsors, authors, or printers.

    Inventory - This is a data store for all the inventory that APC currently has.

    Orders - This is a data store for all the orders that have been placed for APC to print a certain book.

    Contracts - This is a data store for all the contracts that APC has on file. As stated in other documents APC will have several basic contracts that will be constantly used, then there will also be the adapted contracts that have special deals in them that required a change.

    Illustrations/Artwork - This is a data store for all the Illustrations/Artwork that APC has created or bought for certain titles that they are producing.

    Printers - This is a data store for all the different printers that APC has used previously in there business.

    Sponsorship - This is a data store for all the different sponsors that APC has used previously or that have interest in sponsoring a new book.

    Employee's - This is a data store for all the employees at APC. It will be used as a system management data store where all employee information is held to allow credential levels for checks when editing information.



Part 2: Identify the attributes of interest for each entity
  •	Provide a setup/introduction to this section to help the reader understand the importance of getting the right attributes identified through the requirements
  •	Given that you have identified the entities (aka as tables in the database context), identify the attributes of those attributes that you need to store to service the use cases you have identified. Resist the urge to add anything you think might be useful to them in the future. For now just add those attributes that are required to service the requirements.  This is an iterative process in the real world, so you may discover additional attributes later that you missed on the first pass. Just explain why you choose these attributes and relate them to the requirements (RID) they are designed to service. These attributes, plus a primary key, become the attributes you use to populate each table within the ERD.
  •	Create a table to show the data type, length and any constraints for each of the attributes
  •	Provide a summary for the APC reader to make sure they understand the relationship between the attributes and the functional requirements

  In this section APC's attributes for each given entity will be explained and outlined. These attributes will be the variables and content that will fill the entity. Each variable will have a different type of value. In this given case there are only two use values int, which stands for integer, and varchar, which stands for character data. There are also two fields that will be used Throughout the entities, links and info. Links will be a simple link to a document that cant fit in a database field. Info is a common field that will just be there for extra information incase there is important information for that entity that cant be explained by the main fields. These different variables will be assigned to the many entities in the following information:

  Manuscripts
    Title - varchar
    Author - varchar
    ID - int
    Status - varchar
    ISBN - varchar
    Manuscripts Link - varchar

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
    Illustrations/Artwork Link - varchar

  Printers
    Name - varchar
    Average Price - int
    Number Previous Jobs - int
    Info - varchar

  Sponsorship
    Name - varchar
    Average Price - int
    Number Previous Jobs - int
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

  In this section APC's new entities will show the given relationships that they have with other entities. These relationships are how they will communicate and exchange data. In these relationships there are several different ways to communicate. First we have One, then Many, then One(and only one), then zero or one, then one or many, and finally zero or many. These relationships are there to show how one entity will perceive another. For example an entity of "orders" would have a one to one relationship with an entity called "customers" because there can only be one customer per order and there has to be a customer for an order. The entity relationships for APC's entities will be shown in the following information:

  Manuscripts	            1:M	Authors
  Manuscripts	            0:M	Sponsorship
  Manuscripts	            0:M	Contracts
  Manuscripts	            0:M	Printers
  Manuscripts	            0:M	Illustrations/Artwork
  Manuscripts	            0:M	Inventory
  Authors	                0:M	Manuscripts
  Authors	                0:M	Contracts
  Ledger-Cards	          1:M	Accounts
  Ledger-Cards	          0:M	Contracts
  Accounts	              1:1	Ledger-Cards
  Inventory	              0:M	Orders
  Inventory	              1:1	Manuscripts
  Orders	                1:1	Inventory
  Contracts	              0:1	Authors
  Contracts	              0:M	Ledger-Cards
  Contracts	              1:1	Manuscripts
  Illustrations/Artwork	  1:1	Manuscripts
  Printers	              0:M	Manuscripts
  Sponsorship	            0:M	Manuscripts
  Employee's	            1:1	Ledger-Cards


Conclusion
  •	Provide a clear summary of what you learned in the exercise.
  •	Demonstrate your understanding of the purpose and uses of an Entity Relationship Diagram and identify when you would use this tool. Identify how this tool would be used with the stakeholders of the project

  An entity relationship diagram gives a snapshot of how these entities relate to each other. In the diagram, entities are represented by boxes with lines linking them to various attributes, which describe the entity’s qualities or characteristics.

If you use references, put them on a separate reference page with APA formatted references
