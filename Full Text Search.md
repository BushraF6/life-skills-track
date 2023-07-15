# **Full-Text Search** #

## **What is Full-Text Search?** ##

- Full-text search is a technique used in information retrieval that allows searching for documents or data based on the presence of keywords or phrases within the entire text of the document.

### **Why to use it?** ###

- Unlike traditional search methods that rely on simple matching of keywords, full text search takes context, synonyms, and word proximity into account to provide more relevant search results.
- This technique is much faster than string searches for large amounts of data.

### **How does it work?** ###

- Concept behind this technique is indexing.
- Full-text search engines use algorithms to index the content of documents or data sources, and allow users to query the index using natural language queries or Boolean operators to filter and refine results.
- The index then acts as an extensive glossary for any matching documents.

![Overall view of Full-Text Search Concept](https://webimages.mongodb.com/_com_assets/cms/kyxgeyiqchgh6gbmz-image9.gif)

### **Implement Full-Text Search in SQL** ###

- To implement, create a full-text index on each column you want to be indexed.
- In MySQL, this would be done with the FULLTEXT keyword.
- Then you will be able to query the database using MATCH and AGAINST.

  - ALTER TABLE menus ADD FULLTEXT(item);
  - SELECT * FROM menus WHERE MATCH(item) AGAINST("pasta");

<sub>To use features such as fuzzy search, typo tolerance, or synonyms, you will need to add a core search engine such as Apache Lucene on top of your database.
</sub>

### **Application** ###

- Full-text search is commonly used in
  - Databases
  - Search engines
  - Content management systems
  - Other applications that require efficient and accurate searching of large volumes of text-based data.

## **Lucene** ##

- Apache Lucene is an open-source and free program library written in Java.
- It allows its users to add search functionality to an application or website.
- It takes content and adds it to a full-text index which can then be used to perform queries.
- This content, consequently, can be ingested from any number of sources, such as a SQL database or even from the website itself.
- PyLucene is a Python extension for accessing Java Lucene™. Its goal is to allow you to use Lucene's text indexing and searching capabilities from Python.

### **Why Lucene ?** ###

- Lucene can work not only with the Internet, but also with archives, libraries, and PC servers, where it can handle and search HTML documents, e-mail and PDF files.
- Lucene is revolutionary when it comes to incremental indexing, which means that individual entries can be modified, added or removed without the need to do it in batch.

## **Elastic Search** ##

- Elasticsearch is a search engine based on the Lucene library.
- It provides a distributed, multitenant-capable full-text search engine with an HTTP web interface and schema-free JSON documents.

### **Why to use Elastic Search?** ###

- Best suited for
  - Log analytics
  - Full-text search
  - Security intelligence
  - Business analytics
  - Operational intelligence use cases

## **Solr** ##

- Solr is an open-source enterprise-search platform, written in Java.
- Apache Solr is both a search engine and a distributed document database with SQL support.
- Its major features include
  - Full-text search,
  - Hit highlighting,
  - Faceted search
  - Real-time indexing
  - Dynamic clustering
  - Database integration
  - NoSQL features
  - Rich document handling

## **Solr VS Elastic Search** ##

- Both Apache Solr and Elastic‘s Elasticsearch are built on top of Apache Lucene and, therefore, offer similar features and functions.

![Difference between Solr and Elastic Search](https://dattell.com/wp-content/uploads/2020/10/Solr-vs-Elasticsearch-Table3.png)

## **References** ##

- (<https://www.mongodb.com/basics/full-text-search#:~:text=Full%2Dtext%20search%20is%20meant,batch%20indexing%20or%20incremental%20indexing>).
- (<https://techmonitor.ai/technology/data/what-is-apache-lucene>)
- (<https://sematext.com/guides/solr/>)
- (<https://www.knowi.com/blog/what-is-elastic-search/>)
- (<https://youtu.be/upvaxy7zj60>)
