# Mongodb-working-understandings
I have created a basic repository so that all of you can have the knowledge about how the mongoo DB works. 

 🚀 The MongoDB Logic: A "Digital Folder"
The best way to understand MongoDB is to stop thinking about spreadsheets (SQL) and start thinking about folders and files.
1. The Data Hierarchy
In MongoDB, data flows from the broad container down to the specific piece of info:
Database: The physical container (e.g., "Company_DB").
Collection: A folder within that container (e.g., "Employees").
Document: An individual file in that folder (e.g., "John_Doe_Profile").
Field: The actual data inside the file (e.g., Name: "John").
2. Document-Oriented Storage (BSON)
MongoDB stores data in BSON (Binary JSON).
Why BSON? It’s faster for the computer to read than standard text (JSON) and supports more data types (like Date, Long, and Decimal).
Self-Describing: Each document contains its own structure. This means one document can have 5 fields, and the next one in the same collection can have 50.
3. High Availability (The Replica Set)
MongoDB ensures your data is never lost through Replication.
Primary Node: This is the "Boss." All writes (saving data) go here.
Secondary Nodes: These are "Assistants" that constantly mirror the Primary.
Self-Healing: If the Primary server crashes, the Secondaries hold an "election" and automatically promote a new Boss within seconds.
4. Horizontal Scaling (Sharding)
When a database gets too massive for one computer to handle, SQL databases usually require a "bigger computer." MongoDB uses Sharding to grow "sideways."
The Concept: It breaks your huge collection into smaller chunks called Shards.
The Router (mongos): When you ask for data, you talk to a router. It knows exactly which shard holds your data so you don't have to search the whole system.
5. The "No Joins" Philosophy
In traditional databases, you often have to "Join" multiple tables to get a full picture. In MongoDB, you embed data.
SQL way: User Table + Address Table + Orders Table (Joined at runtime).
MongoDB way: One "User Document" that contains the Address and Orders inside it. This makes reading data incredibly fast because the computer only looks in one spot.
💡 Summary for your notes:
Schema-less: Flexible structure for fast-changing data.
Scalable: Built to live on dozens of servers at once.
Developer Friendly: Uses JSON-like syntax that matches modern programming languages.

to get the detaild information you can check out the official website   <br> 🔗
https://www.mongodb.com/docs/
  
