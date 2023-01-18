## Design and implement data stores in a modern data warehouse 

In Synapse, you do not have foreign keys and unique value constraints like you do in SQL Server. Since these rules are not enforced at the database layer, the jobs used to load data have more responsibility to maintain data integrity. You still have the option to use **clustered indexes** but fo rmost dimension tables in Synapse, you'll benefit from using a **clustered column store index (CCI)**.

# Distribution 
Since Synapse Analytics is a **massively parallel processing** (MPP) system, you must consider how data is distributed in your table design. Distribution options include:
- Hash distribution
- Replicated distribution: For smaller tables 
- Round-robin: For staging tables
